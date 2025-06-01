---
layout: post
title: Como baixar arquivos de um servidor FTP com Python e Linux?
excerpt: "Vamos ver como fazer download de vários arquivos de um servidor FTP utilizando Python e Linux?"
categories: [Python, Linux]
comments: true
tag: "Python, Linux"
---

## Apresentação

Dia desses, me deparei com um pequeno problema, acho que algo rotineiro na vida de muitos desenvolvedores e, de certo, usuários Linux. Precisava baixar muitos arquivos de um servidor FTP e não estava nem um pouco a fim de fazer isso de maneira manual. Então, pensando nisso, escrevi um código em Python (versão 3.8), bem simples, que facilitou o download desses arquivos.

No meu caso, precisava realizar o download de toda [base de dados do IBGE](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/15774-malhas.html?=&t=downloads) relativa às malhas territoriais de todos os estados do brasil, compreendendo todos os municípios, da última atualização disponível (ano de 2019).

Nesse processo de desenvolvimento, utilizei Python, como já disse. Pensei em utilizar alguns pacotes externos, como o próprio [Requests](https://requests.readthedocs.io/en/master/) e o [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/), mas regredi e utilizei apenas o pacote padrão da linguagem. Como utilizo Linux, integrei o Python á um comando muito útil dos terminais de distribuições baseadas em Debian chamado [wget](https://www.gnu.org/software/wget/) -- sinceramente, não sei se outras distros já tem o wget pré-instalado.

## Download dos arquivos

Algo simples, como comentei anteriormente. Inicialmente, defini meu interpretador e a codificação utilizada.

```python
#!/usr/bin/env python3.8
# -*- ecoding: utf-8 -*-
```

Em seguida, importei o pacote [os](https://docs.python.org/3/library/os.html) do Python.

```python
import os
```

Depois disso, criei uma variável (url) e, nela, coloquei o caminho do meu diretório FTP.

```python
url = 'ftp://geoftp.ibge.gov.br/organizacao_do_territorio/malhas_territoriais/malhas_municipais/municipio_2019/UFs/'
```

Feito isso, criei uma instância os do sistema, de forma que eu conseguisse executar o comando wget. Como parâmetro do wget, passamos o -r que diz para o comando que executaremos um download recursivo. Em seguida, usando o [format](https://docs.python.org/3/tutorial/inputoutput.html#the-string-format-method), passamos a url de todos os nossos arquivos.

```python
os.system("wget -r {}".format(url))
```

Nosso código ficará assim:

```python
#!/usr/bin/env python3
# -*- ecoding: utf-8 -*-

import os


# Definindo variável com url do diretório de todos os arquivos do servidor FTP.
url = 'ftp://geoftp.ibge.gov.br/organizacao_do_territorio/malhas_territoriais/malhas_municipais/municipio_2019/UFs/'

# Fazendo download de todos os arquivos utilizando o wget do Linux.
os.system("wget -r {}".format(url))
```

Depois de estruturado, vamos executar o programa. No nosso terminal, teremos o seguinte:

![alt](/img/ftp-python-linux.png)

Essas informações indicam, de maneira detalhada, o nome do arquivo que está sendo baixado, bem como para onde ele está sendo encaminhado, seu tamanho etc. Uma observação interessante é a de que, no momento de execução do programa, o wget já se incube da tarefa de organizar nossos diretórios, algo muito útil.

## Concluindo

Esse script foi apenas para praticar um pouco. O comando, utilizando Linux, pode ser executado sem tantos rodeios. Por exemplo:

```shell
wget -r ftp://geoftp.ibge.gov.br/organizacao_do_territorio/malhas_territoriais/malhas_municipais/municipio_2019/UFs/
```

É isso, pessoal. Espero que gostem! <3

Código disponível em: [https://github.com/JacksonOsvaldo/download_malhas_municpio](https://github.com/JacksonOsvaldo/download_malhas_municpio)