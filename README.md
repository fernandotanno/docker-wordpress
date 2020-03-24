# Arquivo base para instalação de Wordpress usando Docker

## Descrição estrutura
Instalação Wordpress utilizando-se da estrategia de containers. Onde sera criado um container para rodar o Wordpress e outro exclusivo para o banco de dados Mysql, esta estrutura permite que caso necessario novas instalaçoes wordpress novos containers sejam criados e compartilhem o mesmo container de banco de dados Mysql. 

## Ambiente para instalação
- Deploy instalação testado em instancia AWS/EC2 | Linux/Ubuntu

## Requisitos
- Docker e Docker-Compose instalado;
- Criar a pasta do projeto "/app/pastas-referentes-ao-volumes/" no server antes do up (nota: implementar criação da estrutura de diretorios no up do container);

## Mapa execução deploy produção e/ou testes
- Passo 1 - Criar instancia AWS/EC2;
- Passo 2 - Acessar instancia AWS/EC2 e atualiza-la;
- Passo 3 - Instalação Docker e Docker-Compose;
- Passo 4 - Criar pasta projeto ( preferencialmente "/app/projeto-wordpress e /app/mysql");
- Passo 5 - Criar as pastas que serão usadas como volume do container (Wordpress e Mysql);
- Passo 6 - Clonar arquivo docker-compose.yml do repositorio Git na pasta do projeto;
- Passo 7 - Executar o comando para criar e executar os containers;
```
docker-compose up
```
- Passo 8 - Verificar se os container forar iniciados com exito:
```
docker-compose ps
```
- Passo 9 - Acessar via navegador o endereço do server para concluir a instalação do wordpress:
```
  Local: http://127.0.0.1:"porta-container-wordpress"
  Externo: http://ip-ou-dominio-instancia-EC2:"porta-container-wordpress"
```
