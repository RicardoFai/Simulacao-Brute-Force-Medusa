# Simulando um Ataque de Brute Force de Senhas com Medusa e Kali Linux

## 📌 Descrição do Projeto
Este projeto documenta a execução prática de testes de auditoria de segurança em um ambiente cibernético simulado e controlado. O objetivo principal é demonstrar a mecânica de ataques de força bruta (*Brute Force*), enumeração de serviços e *Password Spraying*, utilizando o Kali Linux e a ferramenta **Medusa** contra alvos vulneráveis (Metasploitable 2 e DVWA).

---

## 🛠️ Configuração do Ambiente
* **Atacante:** Kali Linux (VirtualBox)
* **Alvo:** Metasploitable 2 (VirtualBox)
* **Rede:** Configurada em **Placa em Modo Bridge** (*Bridged Adapter*), permitindo a comunicação em camada L2/L3 entre as máquinas virtuais sob o mesmo segmento de rede (`192.168.2.x`).

---

## 🚀 Etapas Executadas e Comandos

### 1. Reconhecimento e Validação de Rede
Validação de conectividade e varredura de portas abertas nos serviços alvo (FTP, SSH, HTTP, SMB):

```bash
# Teste de conectividade ICMP
ping -c 3 192.168.2.111

# Varredura de versão de serviços via Nmap
nmap -sV -p 21,22,80,139,445 192.168.2.111
