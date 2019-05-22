# Docker Compose - Ambiente de Desenvolvimento para aplicativos Nextcloud

## Sobre

Essa composição foi formada para que possamos ter um ambiente de desenvolvimento para plugins e aplicativos que possam ser executados na plataforma nextcloud.

A composição foi formada com seis imagens disponíveis em https://hub.docker.com, sendo mantidas respectivamente por seus desenvolvedores.

## Como baixar e instalar este Docker-Compose

Clone o repositório em uma pasta de usuário do seu sistema operacional com os seguintes comandos no terminal:

`` `txt
git clone https://github.com/github/VisualStudio
cd nextcloud
`` `

Logo após, para baixar as imagens e criar seu container execute o seguintes comando.

`` `txt
docker-compose up -d
`` `

Aguarde até de todos os pacotes de imagens sejam baixados e instalados no docker.

## Como acessar e usar o nextcloud através do docker

Após finalizar a instalação dos seis containers serão apresentados os nomes dos mesnos com a palavra `done`,
isso significa que foi concluida com sucesso a instalação. 

Aguarde um ou dois minutos, para que o docker possa criar os arquivos do Nextcloud dentro da pasta 
`nextcloudFiles` dentro do diretório do usuário. Se desejar, abra esta pasta e verifique se já foi concluida 
a cópia dos 25 arquivos e pastas.

### Acessando o Nextcloud

Abra seu navegador e aplique a sequinte URL

(http://localhost:8080)

> Nota: Se não apresentar nada, significa que os arquivos do nextcloud ainda não foram copiados completamente.

## Confiruação inicial do ambiente Nextcloud

No primeiro acesso, será solicitado Login e Senha, estes são o Usuário Root e sua senha, crie um nome e uma senha para o mesmo, exemplo  `admin`,  `MinhaSenhaSegura123`.

Escolha o banco de dados que será usado, Este ambiente está preparado para o uso do Postgres.

Na configuração do Banco de dados Postgres:
Nome do usuário: `nextcloud`
Senha do banco: `nextcloud`
Nome do banco: `nextcloud_db`
host: `db`

### Acessando do banco de dados e suas tabelas

Para acessar o PgAdmin, abra seu navegador e aplique a sequinte URL

(http://localhost:8888)

Informe o login `admin@admin` e a senha `admin`

### Acessando os arquivos do Nextcloud por FTP

Baixe algum aplicativo de ClienteFTP e configure o acesso com os seguintes dados:

Protocolo: `FTP`
Host: `localhost`
Porta: `2121`
Tipo de login: `Normal`
Usuário: `nextcloud`
Senha: `nextcloud`
