<!-- TITLE: Docker -->
<!-- SUBTITLE: Manual para a utilização do Docker -->


# Lista de comandos

| Comando                               | Descrição                                                                                                                                                                                                | |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |-|
| _docker ps_                                                                                                                                 |  Exibe todos os containers em execução no momento.   ||
| _docker ps -a_                                                                                                                             |  Exibe todos os containers, independente de estarem em execução ou não.   ||
|  _docker run -it NOME_DA_IMAGEM_                                                                                        |  Conecta o terminal que estamos utilizando com o do container.  ||
|  _docker start ID_CONTAINER_                                                                                                 |  Inicia o container com id em questão.   ||
| _docker stop ID_CONTAINER_                                                                                                  |  Interrompe o container com id em questão.   ||
| _docker start -a -i ID_CONTAINER_                                                                                          |   Inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.  ||
| _docker rm ID_CONTAINER_                                                                                                    |  Remove o container com id em questão.    ||
|  _docker container prune_                                                                                                        |  Remove todos os containers que estão parados.              ||
|  _docker rmi NOME_DA_IMAGEM_                                                                                             |   Remove a imagem passada como parâmetro.              ||
|  _docker run -d -P --name NOME dockersamples/static-site_                                                    |  Ao executar, dá um nome ao container.              ||
|  _docker run -d -p 12345:80 dockersamples/static-site_                                                           |  Define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.  ||
|  _docker run -d -e AUTHOR="Fulano" dockersamples/static-site_                                            |   Define uma variável de ambiente AUTHOR com o valor Fulano no container criado.   ||
|  _docker run -p 8080:3000 -v "$(pwd):/var/www" -w "/var/www" node npm start_                  |   Rodar node.   ||
|  _docker build -f Dockerfile_                                                                                                       | Cria uma imagem a partir de um Dockerfile.   ||
|  _docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM_                                            |   Constrói e nomeia uma imagem não-oficial.    ||
|  _docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM CAMINHO_DOCKERFILE_     |   Constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.   ||
|  _docker login_                                                                                                                             |   Inicia o processo de login no Docker Hub.   ||
|  _docker push NOME_USUARIO/NOME_IMAGEM_                                                                     |   Envia a imagem criada para o Docker Hub.   ||
|  _docker pull NOME_USUARIO/NOME_IMAGEM_                                                                       |   Baixa a imagem desejada do Docker Hub.    ||
|  _docker network create --driver bridge minha-rede_                                                                  |   Cria nova REDE   ||
|  _docker run -it --name meu-container-de-ubuntu --network minha-rede ubuntu_                   |   Rodando Container na REDE criada   ||
|  _docker-compose build_                                                                                                             |   Executa os steps do docker compose   ||
|  _docker-compose up_                                                                                                                  |  Sobe os serviços   ||
|  _docker-compose down_                                                                                                            |   Finaliza os serviços   ||

