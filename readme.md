# SonarQube


1.  Certifique-se de ter o Docker e o Docker Compose instalados no servidor. Se não estiverem instalados, siga as instruções adequadas para a instalação em seu sistema operacional.
    
2.  Crie um novo diretório em seu servidor onde deseja armazenar os arquivos do Docker Compose. Por exemplo, você pode criar um diretório chamado "sonarqube" usando o comando `mkdir sonarqube`.
    
3.  Dentro do diretório recém-criado, crie um arquivo chamado "docker-compose.yml" e abra-o em um editor de texto.
    
4.  Copie o conteúdo do exemplo de arquivo Docker Compose fornecido e cole-o no arquivo "docker-compose.yml" que você acabou de criar.
    
5.  Salve e feche o arquivo "docker-compose.yml".
    
6.  Abra um terminal ou uma janela de linha de comando e navegue até o diretório onde você criou o arquivo "docker-compose.yml".
    
7.  Execute o comando `docker-compose up -d`. Isso iniciará o processo de construção e execução dos contêineres conforme definido no arquivo Docker Compose. O parâmetro "-d" é opcional e permite que os contêineres sejam executados em segundo plano (modo "detached").
    
8.  Aguarde enquanto o Docker baixa as imagens necessárias e cria os contêineres. Esse processo pode levar algum tempo dependendo da velocidade da conexão com a Internet e do desempenho do servidor.
    
9.  Uma vez que o Docker tenha concluído a criação dos contêineres, você pode verificar se eles estão em execução usando o comando `docker ps`. Isso mostrará uma lista dos contêineres em execução no servidor.
    
10.  Se os contêineres estiverem em execução corretamente, você poderá acessar o SonarQube em seu navegador usando o endereço IP ou o nome de domínio do servidor, seguido pela porta 9000. Por exemplo, se o servidor tiver o endereço IP 192.168.0.1, você pode acessar o SonarQube digitando "[http://192.168.0.1:9000](http://192.168.0.1:9000/)" no navegador.
    
11.  Para parar e remover os contêineres, execute o comando `docker-compose down` no mesmo diretório onde você executou o comando "docker-compose up".
    

12.  E por ultimo, para testar seu repositorio:

`docker run --rm -e SONAR_HOST_URL="https://seuip:9000" -e SONAR_TOKEN=1234 -v "$(pwd):/usr/src" sonarsource/sonar-scanner-cli`


Lembre-se de adaptar o exemplo de arquivo Docker Compose e sonar-project de acordo com suas necessidades, como definir senhas e outros parâmetros de configuração. Além disso, certifique-se de ter as dependências corretas instaladas no servidor, como o Docker e o Docker Compose, antes de iniciar o processo de implantação.