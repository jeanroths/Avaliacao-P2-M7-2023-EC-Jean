# Template para avaliação P2

Saída esperada após execução do programa:

<img src="./media/tela-front.png" display="flex">

# IMPORTANTE:

Para colocar o frontend para funcionar, colocar uma máquina EC2 rodando o Apache WebServer.
Para isso, instalar dentro da EC2:

```bash
sudo apt update
sudo apt upgrade
sudo apt install apache2
# os arquivos do projeto devem estar em /var/www/html
git clone https://github.com/Murilo-ZC/Avaliacao-P2-M7-2023-EC.git
sudo cp ./Avaliacao-P2-M7-2023-EC/frontend /var/www/html
```

Aqui pessoal, os arquivos já estaram disponíveis na porta 80, não necessário redirecionar.

> IMPORTANTE: Verificar as rotas e utilziar o seu próprio repositório com as modificações realizadas.


# Solução

Para fazer a solução eu criei um EC2 front e outro EC2 para o backend, nisso eu clonei esse repositório nas duas instâncias uma em que eu subiria o servidor e outro em que eu usei o Apache.

## Frontend
 Para o frontend eu fiz o que foi orientado de usar o apache e coloquei no diretorio /var/www/html/p2front, e substitui o ip das rotas pelo ip elástico do backend.

## Backend
substitui as configurações do RDS pelo database que eu criei.

## RDS e EC2
Para criação dos ECs usei t2.micro e ubuntu, configurei os IPs elásticos para cada um dos dois ECs. Para o RDS alterei a segurança com configuração de entrada e coloquei host, url e senha no backend.