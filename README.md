# medusa-test-metasploitable2-vm
teste de força bruta no metasploitable2 a partir do kali com medusa

<img width="1904" height="1074" alt="projeto em execução" src="https://github.com/user-attachments/assets/6e9ada02-6daa-4d16-85c5-6a092def2234" />

Resumo do aprendizado (tópicos)
1. Configuração de ambiente
Criação de laboratório isolado com VirtualBox (rede host-only).
Integração entre máquinas vulneráveis e máquina atacante.
Importância do isolamento para testes éticos e seguros.
2. Fundamentos de ataques de força bruta
Diferença entre:
Brute force clássico (todas combinações)
Dictionary attack (wordlists)
Password spraying (uma senha para vários usuários)
Impacto da complexidade de senha no tempo de ataque.
3. Uso da ferramenta Medusa
Estrutura de comandos por protocolo (FTP, SMB, HTTP).
Uso de parâmetros para paralelismo e otimização.
Integração com listas de usuários e senhas.
4. Exploração de serviços vulneráveis
FTP: autenticação sem proteção contra múltiplas tentativas.
SMB: enumeração de usuários + spraying.
Web (DVWA): automação de login via requisições HTTP.
5. Wordlists e estratégia de ataque
Criação de listas simples e direcionadas.
Eficiência maior com dados contextualizados (nomes comuns, padrões).
Relação entre tamanho da lista e tempo de execução.
6. Validação de acessos
Identificação de credenciais válidas via resposta do serviço.
Confirmação manual após descoberta.
Importância de evitar falsos positivos.
7. Medidas de mitigação
Políticas de senha forte (comprimento, complexidade).
Rate limiting / bloqueio após tentativas.
Implementação de MFA (autenticação multifator).
Monitoramento de logs e alertas.
Desativação de serviços desnecessários.
8. Visão prática de segurança ofensiva
Entendimento real de como ataques são executados.
Correlação direta entre vulnerabilidade e exploração.
Base para atuação defensiva mais eficiente (Blue Team).
