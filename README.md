# Rodando o Projeto Vue com Docker

Este projeto utiliza Docker para facilitar a execução do aplicativo Vue.js em um ambiente de contêiner.

## Pré-requisitos

Certifique-se de ter o Docker instalado em sua máquina antes de prosseguir. Você pode baixar e instalar o Docker a partir do site oficial: [Docker Website](https://www.docker.com/get-started)

## Instruções de Uso

Siga os passos abaixo para construir e executar o aplicativo Vue.js em um contêiner Docker:

1. **Construir a imagem Docker**:

   Abra um terminal e navegue até o diretório raiz do seu projeto Vue.

   Execute o seguinte comando para construir a imagem Docker:

   ```
   docker build -t vue-image .
   ```

2. **Executar o contêiner Docker**:

Após a construção bem-sucedida da imagem Docker, execute o seguinte comando para iniciar o contêiner:

```
docker run -it -p 8080:80 --name vue-docker vue-image
```

Este comando executa o contêiner e mapeia a porta 80 do contêiner para a porta 8080 do host local.

3. **Acessar a aplicação Vue**:

Abra um navegador da web e acesse `http://localhost:8080` para visualizar sua aplicação Vue sendo executada no contêiner Docker.

## Observações

- Certifique-se de que nenhum outro serviço esteja sendo executado na porta 8080 do seu host local antes de iniciar o contêiner Docker.
- Se você deseja alterar o nome da imagem Docker ou o nome do contêiner, substitua "vue-image" e "vue-docker" pelos nomes desejados nos comandos acima.
