# spfbl-web-client

Simples interface para gerenciamento SPFBL. A ideia é ter uma interface web que proporcione ao usuário final (destinatário) o gerenciamento de suas mensagens.

# Instalação

OBS: Este programa deve ser instalado no host onde o SPFBL é executado ou ter acesso direto aos arquivos de LOG

Clone:

```
git clone https://github.com/ncaio/spfbl-web-client.git
```
Arquivo de configuração:

```
cd /etc
ln -s /caminho/spfbl-web-client/spfbl-web-client.toml
```
ou
```
cp spfbl-web-client.toml /etc
```

Execução:

./spfbl-web-client


# Dependências

Esta app é desenvolvida na linguagem Go e para utilizar a partir do código fonte, precisa de:
```
go get github.com/pelletier/go-toml
```
# Arquivo de configuração

É preciso que o arquivo /etc/painel-spfbl.toml exista e seja acessível pelo spfbl-web-client

Exemplo de arquivo:

```
[org]
organizationname = "Nome da organizacao"
organizationdescription = "Breve descritivo da instituicao"
[server]
hostname = "hostname.domain.tld"
host = "localhost"
port = "9877"
[mail]
admin = "postmaster@domain.tld"
[log]
path = "/var/log/spfbl/"
```
A principio, as variáveis "hostname" e "path" são as principais e as únicas que requerem modificação. 
Onde:
hostname = a variável hostname existente em seu arquivo spfbl.conf
path = Caminho dos logs SPFBL
