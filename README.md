&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Lambda](https://cloudacademy.com/wp-content/uploads/2016/07/AWS-Lambda-1.jpg "AWS Lambda")

# &emsp;&nbsp;Projeto base para função lambda na plataforma AWS

O projeto é uma função (p/ Serviço Lambda - AWS) que trabalha em conjunto com o serviço de armazenamento S3 e o serviço de banco de dados não relacional (NoSQL) DynamoDB.

Ao ser carregado qualquer arquivo no serviço S3, automaticamente a função lambda é disparada (o evento gatilho vem do S3). A função então analisa o arquivo (um arquivo de texto), efetua o *parse* do mesmo para um JSON e o salva no serviço DynamoDB, similar ao que é mostrado na imagem abaixo (com exceção de o arquivo de entrada ser uma imagem e o usuário poder listar as mesmas):

![Lambda 2](http://blog.michaelschmatz.com/images/image-host.png "Funcionamento do projeto, considerar que os uploads são arquivos de texto JSON")
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;*Funcionamento do projeto, considerar que os uploads são arquivos de texto não imagens*

Exemplo de conteúdo de um arquivo de texto (JSON) para upload no S3:  
*{  
&emsp;&emsp;"invoiceNumber": "INV_1234",  
&emsp;&emsp;"customerName": "a name",  
&emsp;&emsp;"totalValue": 1250.00,  
&emsp;&emsp;"productId": 1,  
&emsp;&emsp;"quantity": 3  
}*  

Adicionalmente, logs são gerados no CloudWatch.

Projeto feito na disciplina **DM123 - Desenvolvimento de aplicações com segurança no ambiente Amazon Web Services**, durante o curso de **Pós graduação no INATEL - Instituto Nacional de Telecomunicações**.

&emsp;

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**Mais informações sobre AWS Lambda:** https://aws.amazon.com/pt/lambda/
