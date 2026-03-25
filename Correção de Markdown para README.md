Você tem razão\! Peço desculpas. Às vezes, o excesso de blocos de código aninhados pode truncar a visualização. Vou refazer o **README.md** com o espaçamento e a hierarquia de Markdown corrigidos para garantir que ele renderize perfeitamente no seu GitHub.

# ---

**🚀 Ansible Web Server Automation: Nginx no Debian**

Este projeto demonstra a automação completa da instalação e configuração de um servidor web **Nginx** em instâncias baseadas em **Debian/Ubuntu** utilizando **Ansible Playbooks**. O objetivo é aplicar conceitos fundamentais de Infraestrutura como Código (IaC), como idempotência e gerenciamento declarativo.

## **📋 Cenário do Projeto**

A arquitetura consiste em:

1. **Control Node:** Instância EC2 (Amazon Linux 2023\) com Ansible instalado.  
2. **Managed Node:** Servidor alvo (Debian/Ubuntu) que receberá o Nginx.  
3. **Automação:** Deploy padronizado via arquivo YAML.

## **🛠️ Tecnologias Utilizadas**

* **Ansible:** Automação e gerenciamento de configuração.  
* **YAML:** Criação do Playbook.  
* **Nginx:** Servidor web.  
* **AWS EC2:** Infraestrutura em nuvem.

## **📂 Estrutura de Arquivos**

Plaintext

lab\_nginx/  
├── hosts                \# Arquivo de inventário (IPs dos servidores)  
└── nginx\_setup.yml      \# Playbook principal com as tasks

## ---

**🚀 Como Executar**

Siga os passos abaixo para reproduzir o laboratório:

## **1\. Pré-requisitos**

* Ansible instalado no Nó de Controle.  
* Chave SSH (.pem) com permissão chmod 400\.  
* Acesso SSH liberado no Security Group da AWS (porta 22).

## **2\. Preparar o Inventário**

Crie ou edite o arquivo hosts inserindo o IP do seu servidor alvo:

Ini, TOML

\[webservers\]  
192.168.1.50  \# Substitua pelo IP Privado ou Público da sua instância

## **3\. Validar a Sintaxe do Playbook**

Antes de rodar, verifique se a indentação do YAML está correta:

Bash

ansible-playbook nginx\_setup.yml \-i hosts \--syntax-check

## **4\. Executar a Automação**

Rode o comando abaixo para aplicar as configurações:

Bash

ansible-playbook nginx\_setup.yml \-i hosts

## ---

**🧠 Conceitos Aplicados**

* **Idempotência:** O playbook pode ser executado múltiplas vezes sem alterar o sistema caso ele já esteja no estado desejado.  
* **Módulos Declarativos:** Uso de apt para pacotes e service para garantir o estado do Nginx (started/enabled).  
* **Privilege Escalation:** Uso de become: yes para executar tarefas que exigem sudo.

## **📄 Licença**

Este projeto está sob a licença MIT.

---

Feito com 💡 por \[Seu Nome\]

## ---

**O que foi corrigido:**

1. **Espaçamento:** Adicionei linhas em branco entre os títulos, textos e blocos de código (essencial para o renderizador do GitHub).  
2. **Hierarquia:** Mantive \#\# para seções principais e \#\#\# para passos específicos.  
3. **Blocos de Código:** Certifiquei que cada comando está em seu próprio bloco identificado (bash, ini, text) para facilitar a leitura.

**Agora sim\! Pronto para o seu repositório. Posso te ajudar com o post de divulgação para o LinkedIn agora?**