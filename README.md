# Docker Images Collection

Este repositório contém diversas configurações de contêineres Docker organizadas por serviço. Cada pasta possui os arquivos necessários para configurar e executar a respectiva imagem.

## Índice
- [Visão Geral](#visao-geral)
- [Requisitos](#requisitos)
- [Configuração](#configuracao)
- [Serviços Disponíveis](#servicos-disponiveis)
- [Comandos útis](#comandos-uteis)
- [Contribuição](#contribuicao)

## Visão Geral
Este repositório facilita a inicialização e gerenciamento de contêineres Docker para diversos serviços populares, permitindo a execução local para desenvolvimento, testes e aprendizado.

## Requisitos
Antes de iniciar, certifique-se de ter os seguintes requisitos instalados:
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Configuração
1. Clone o repositório:
   ```bash
   git clone git@github.com:iKaueMatos/docker-images.git
   cd docker-images
   ```
2. Navegue até a pasta do serviço desejado e execute:
   ```bash
   docker-compose up -d
   ```
   ou, caso não tenha um `docker-compose.yml`, utilize:
   ```bash
   docker build -t nome-da-imagem .
   docker run -d --name nome-do-container nome-da-imagem
   ```

## Serviços Disponíveis
Cada pasta representa um serviço Docker que pode ser utilizado:

- **grafana** - Monitoramento e visualização de métricas
- **keycloak** - Gerenciamento de identidade e acesso
- **mongodb** - Banco de dados NoSQL orientado a documentos
- **mongodb_and_node** - Integração entre MongoDB e Node.js
- **mysql_and_node** - Integração entre MySQL e Node.js
- **nginx** - Servidor web reverso e proxy
- **php_and_mysql** - Configuração de ambiente para desenvolvimento PHP com MySQL
- **portainer** - Interface web para gerenciamento de contêineres Docker
- **rabbitmq** - Mensageria baseada em filas
- **sonarqube** - Análise de qualidade de código

## Comandos ## Comandos \uteis
### Listar contêineres em execução
```bash
docker ps
```

### Parar um contêiner
```bash
docker stop nome-do-container
```

### Remover um contêiner
```bash
docker rm nome-do-container
```

### Construir uma imagem
```bash
docker build -t nome-da-imagem .
```

### Executar um contêiner interativamente
```bash
docker run -it nome-da-imagem /bin/bash
```

### Acessar logs de um contêiner
```bash
docker logs -f nome-do-container
```

## Contribuição
Sinta-se à vontade para abrir um Pull Request ou relatar problemas na seção de issues do repositório.

