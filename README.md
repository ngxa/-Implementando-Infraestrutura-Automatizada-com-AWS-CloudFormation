# -Implementando-Infraestrutura-Automatizada-com-AWS-CloudFormation

Acesso ao Console AWS

Passos realizados:
Login: Acessei console.aws.amazon.com
Região: Confirmada us-east-1 (N. Virginia)
Serviços: Naveguei para CloudFormation

Verificação via Console
No Console CloudFormation:
Stack meu-servidor-web listada com status CREATE_COMPLET
Visualizei recursos criados: EC2 Instance e Security Group
Verifiquei eventos da stack
Instância EC2 criada com tag "Infraestrutura_Automatizada"
Security Group com regra porta 80
Estado: Running

Acesso ao GITBASH
aws configure
Configurações usadas:
AWS Access Key ID: [minha access key]
AWS Secret Access Key: [minha secret key]
Default region: us-east-1 (Virginia do Norte)
Default output format: json

aws configure get region
Para verificar se o template é válido
aws cloudformation validate-template --template-body file://criar_ec2.json
Para fazer o Deploy:
aws cloudformation create-stack \
  --stack-name meu-bucket-s3 \
  --template-body file://templates/criar_ec2.json

Da mesma forma pude criar um Bucket S3 (criar_S3.json)
 
 
