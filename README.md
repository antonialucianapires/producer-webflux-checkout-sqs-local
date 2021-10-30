# Localstack + Webflux: Criando um producer SQS localmente

Projeto criado durante uma das apresentações da plataforma Expert Clubs ministrada pela [Kamila Santos](https://github.com/Kamilahsantos).

#### Tecnologias utilizadas
Spring Webflux, Localstack, AWS SDK, AWS CLI, SQS e Docker

#### Ambiente 
- Subir o container localstack com o sqs 


  ````
  docker-compose up
  ````
  
 - Criar fila SQS


  ````
   aws --endpoint-url=http://localhost:4566 sqs create-queue --queue-name process-order-queue
  ````
  
 - Criar mensagens na fila


  ````
   curl --location --request POST 'http://localhost:8080/checkout/create-payment
  ````
