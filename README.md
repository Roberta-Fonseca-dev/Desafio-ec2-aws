# Gerenciamento de Instâncias EC2 na AWS  

Este repositório foi criado como parte do desafio da **DIO (Digital Innovation One)** para consolidar conhecimentos em **gerenciamento de instâncias EC2 na AWS**.  

---

## 📌 Objetivo  
Aplicar na prática os conceitos aprendidos sobre criação, configuração e gerenciamento de instâncias **EC2 na AWS**, documentando a experiência e os aprendizados adquiridos.  

---

## 🖥️ Passos Realizados  

1. **Acesso ao Console AWS**  
   - Login no [AWS Management Console](https://aws.amazon.com/console/).  
   - Navegação até o serviço **EC2**.  

2. **Criação da Instância EC2**  
   - Escolha da **AMI (Amazon Machine Image)**: Amazon Linux 2.  
   - Seleção do tipo de instância: `t2.micro` (Free Tier).  
   - Configuração de segurança (Security Group) permitindo acesso SSH (porta 22) e HTTP (porta 80).  

3. **Acesso à Instância**  
   - Download da chave `.pem`.  
   - Conexão via terminal usando:  
     ```bash
     ssh -i "minha-chave.pem" ec2-user@<ip-da-instancia>
     ```  

4. **Configuração do Servidor**  
   - Atualização dos pacotes:  
     ```bash
     sudo yum update -y
     ```  
   - Instalação do servidor Apache:  
     ```bash
     sudo yum install httpd -y
     sudo systemctl start httpd
     sudo systemctl enable httpd
     ```  
   - Página de teste criada em `/var/www/html/index.html`.  

5. **Teste no Navegador**  
   - Acesso via `http://<ip-publico-da-instancia>` para verificar o funcionamento do Apache.  

---

## 📷 Evidências  

Imagens de apoio estão na pasta [`/images`](./images) (prints do console AWS e da instância em execução).  

---

## 📚 Aprendizados  

- Entendi a diferença entre **AMI** e **tipo de instância**.  
- Configurei regras de segurança básicas usando **Security Groups**.  
- Aprendi a acessar a instância via **SSH** e instalar pacotes no servidor.  
- Ganhei prática em **documentar processos técnicos** usando Markdown.  

---

## 🔗 Recursos Úteis  

- [Documentação oficial do Amazon EC2](https://docs.aws.amazon.com/pt_br/ec2/index.html)  
- [Guia rápido do GitHub](https://docs.github.com/pt/get-started/quickstart)  
- [Guia Markdown no GitHub](https://guides.github.com/features/mastering-markdown/)  

---

## 🚀 Conclusão  

Este desafio foi fundamental para colocar em prática os conceitos aprendidos sobre **instâncias EC2**. A experiência de criar, configurar e documentar o processo reforçou meu entendimento de como funciona a infraestrutura em nuvem da AWS.  
