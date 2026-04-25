# medusa-test-metasploitable2-vm
teste de força bruta no metasploitable2 a partir do kali com medusa

<img width="1904" height="1074" alt="projeto em execução" src="https://github.com/user-attachments/assets/6e9ada02-6daa-4d16-85c5-6a092def2234" />


🔐 Projeto Prático: Testes de Força Bruta com Kali Linux e Medusa
📌 Objetivo


Implementar, documentar e demonstrar ataques simulados de força bruta utilizando o Kali Linux e a ferramenta Medusa em ambientes vulneráveis como Metasploitable 2 e DVWA, com foco em análise prática e aplicação de medidas de mitigação.


🧱 Estrutura do Ambiente
🔧 Ferramentas utilizadas
Kali Linux (máquina atacante)
Metasploitable 2 (máquina vulnerável)
DVWA (aplicação web vulnerável)
VirtualBox
🌐 Configuração de rede
Tipo: Host-Only
Comunicação isolada entre VMs
Sem acesso externo (ambiente controlado)
⚙️ Cenários de Ataque Simulados
1. 🔓 Força Bruta em FTP

Objetivo: Descobrir credenciais válidas no serviço FTP.

Exemplo de comando:

medusa -h <IP_ALVO> -u msfadmin -P wordlist.txt -M ftp

Resultado esperado:

Identificação de login válido
Acesso ao serviço FTP
2. 🌐 Ataque a Login Web (DVWA)

Objetivo: Automatizar tentativas de login via formulário web.

Abordagem:

Interceptação da requisição (Burp Suite ou navegador)
Repetição com variações de senha

Exemplo de uso com Medusa (HTTP):

medusa -h <IP_ALVO> -u admin -P wordlist.txt -M http -m FORM:"/dvwa/login.php:username=^USER^&password=^PASS^:F=Login failed"
3. 🗂️ Password Spraying em SMB

Objetivo: Testar uma senha comum contra múltiplos usuários.

Exemplo de comando:

medusa -h <IP_ALVO> -U users.txt -p senha123 -M smbnt

Técnica aplicada:

Enumeração de usuários
Teste de senha única em larga escala
📄 Wordlists Utilizadas

Exemplo simples:

123456

password

admin

msfadmin

senha123

Observação:

Listas pequenas para testes rápidos
Em cenários reais, usar listas maiores e contextualizadas

✅ Validação de Resultados
Identificação de credenciais válidas via output do Medusa
Teste manual de autenticação
Registro de sucessos e falhas

🛡️ Medidas de Mitigação

🔐 Políticas de senha forte

⛔ Bloqueio após múltiplas tentativas

🧠 Autenticação multifator (MFA)

📊 Monitoramento de logs

🔕 Desativação de serviços desnecessários

📚 Conclusão

Os testes demonstraram que sistemas sem proteção adequada são rapidamente comprometidos por ataques automatizados. O uso do Medusa evidenciou a importância de controles básicos de segurança, como limitação de tentativas e uso de senhas robustas.

A prática em laboratório com Metasploitable 2 e DVWA permitiu compreender, de forma aplicada, a relação entre vulnerabilidade e exploração.

📖 Aprendizados (Resumo)

📌 Configuração de ambiente isolado

📌 Tipos de ataque (brute force, dictionary, spraying)

📌 Uso prático do Medusa

📌 Exploração de serviços reais (FTP, SMB, HTTP)

📌 Criação e uso de wordlists

📌 Validação de credenciais

📌 Implementação de medidas defensivas

📌 Visão prática de segurança ofensiva

⚠️ Aviso

Este projeto foi realizado em ambiente controlado para fins educacionais.
Não utilize essas técnicas em sistemas sem autorização.
