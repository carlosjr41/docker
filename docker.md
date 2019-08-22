<!-- TITLE: Docker -->
<!-- SUBTITLE: Manual para a utilização do Docker -->


# Download
1. Ir ao site: https://docs.docker.com/docker-for-windows/install/ e baixar o instalador do Docker.
	
	![1 1](/uploads/docker/1-1.png "1 1")

# Instalação
1. Início da Instalação Docker para Windows após clicar no instalador.

	![001](/uploads/docker/001.png "001")
	
2. Configuração (não marcar as opções nesta etapa, apenas OK na parte inferior da tela).

	![002](/uploads/docker/002.png "002")
	
3. Instalação dos arquivos. 

	![003](/uploads/docker/003.png "003")
	
4. Instalação realizada com sucesso (clicar no Close and Log out).

  ![004](/uploads/docker/004.png "004")
	
5. Clicar no ícone do Docker em "Mostrar Ícones Ocultos" na barra de Tarefas.

	![005](/uploads/docker/005.png "005")
	
6. Clicar em OK para reinicar o computado para completar a instalação.

	![006](/uploads/docker/006.png "006")
	
7. Tela de login.

	![007](/uploads/docker/007.png "007")
	
8. Vericando a instalação através do Prompt de Comando.

    ![008](/uploads/docker/008.png "008")


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

