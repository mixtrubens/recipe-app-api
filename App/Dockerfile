#Versão do python utilizada no container(Simple tag).
FROM python:3.7-alpine
# No projeto original era usado  "MAINTAINER <nome do autor>"
#Porém essa tag foi depreciada.
#Autor da imagem/Organização
LABEL maintainer="rubens.vieira@br.ey.com"
#Variável de ambiente para executar o python sem buffer
ENV PYTHONUNBUFFERED 1
#Irá copiar as bibliotecas escritas no arquivo txt.
COPY ./requirements.txt /requirements.txt
#Instala as bibliotecas copiadas
RUN pip install -r /requirements
#Cria a pasta APP
RUN mkdir /
#Defini app como diretório principal.
WORKDIR /app
COPY ./app /app
#criação de um usuário apenas para executar o
RUN adduser -D user
USER user
