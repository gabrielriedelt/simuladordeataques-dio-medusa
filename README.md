# simuladordeataques-dio-medusa
Exemplos de ataques para descobrir usuários e senhas utilizando Medusa e Metasploitable no Kali Linux
🔐 Simulação de Ataques com Kali Linux, Medusa e Metasploitable

Este repositório documenta atividades práticas realizadas em laboratório controlado com foco em testes de intrusão (Pentest) e segurança ofensiva, utilizando ferramentas amplamente empregadas na área de cibersegurança.

🎯 Objetivo

O objetivo deste projeto foi simular cenários reais de ataque para:

Identificar serviços expostos em rede
Enumerar usuários válidos
Realizar testes de força bruta em serviços
Validar credenciais comprometidas
Compreender falhas de configuração e segurança

Todo o ambiente foi executado de forma controlada e legal, utilizando máquinas vulneráveis como o Metasploitable.

🛠️ Ferramentas Utilizadas
Kali Linux
Medusa (ferramenta de brute force)
Metasploitable 2 (máquina vulnerável)
SMBClient (enumeração de compartilhamentos SMB)
FTP (acesso remoto a arquivos)
DVWA (Damn Vulnerable Web Application)


🧪 Atividades Realizadas:


🔎 Enumeração de Serviços (SMB)

Foi realizada a enumeração de compartilhamentos SMB utilizando:

smbclient -L //192.168.56.101 -U msfadmin

Com isso, foi possível identificar:

Compartilhamentos disponíveis
Estrutura de diretórios
Indícios de configurações vulneráveis


🔑 Ataque de Força Bruta com Medusa (FTP)

Utilizando a ferramenta Medusa, foram realizados ataques de força bruta contra o serviço FTP:

medusa -h 192.168.56.101 -U user.txt -P pass.txt -M ftp -t 6

Resultados obtidos:

Identificação de credenciais válidas
Descoberta do usuário msfadmin
Senha encontrada com sucesso via brute force


📂 Acesso ao Serviço FTP

Após a descoberta das credenciais, foi possível autenticar no servidor:

ftp 192.168.56.101

Resultado:

Login bem-sucedido no servidor FTP
Confirmação da vulnerabilidade de credenciais fracas
Possibilidade de acesso a arquivos remotos


🌐 Exploração Web com DVWA

Também foram realizados testes na aplicação vulnerável DVWA, incluindo:

Exploração de falhas de autenticação
Testes de força bruta
Análise de vulnerabilidades web comuns


No fim, conhecimentos Adquiridos:

Durante este laboratório, foram desenvolvidas habilidades em:

Enumeração de serviços de rede
Ataques de força bruta
Exploração de serviços mal configurados
Identificação de credenciais fracas
Uso prático de ferramentas de Pentest
Interpretação de respostas de serviços (SMB, FTP)

⚠️ Aviso Legal

Este projeto foi realizado exclusivamente para fins educacionais, em ambiente controlado.
Nenhuma atividade foi executada contra sistemas reais sem autorização.
