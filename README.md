# Projeto de Infraestrutura de Rede para Cooperativa Bancária

## 📘 Visão Geral do Projeto

Este projeto acadêmico foi desenvolvido na disciplina de Redes de Computadores com o objetivo de simular uma infraestrutura de rede para uma cooperativa bancária fictícia, localizada em Goiás, Brasil. Ele conecta três agências — Goiânia (Matriz), Anápolis e Catalão — utilizando boas práticas de endereçamento, roteamento e segurança.

> 💡 **Objetivo**: Demonstrar o domínio de conceitos essenciais de redes de computadores na prática, usando o Cisco Packet Tracer.

---

## 🛠 Tecnologias Utilizadas

- Cisco Packet Tracer
- Protocolo DHCP
- NAT com sobrecarga (PAT)
- Roteamento Estático
- Sub-redes com VLSM
- Conectividade via links seriais (DTE/DCE)

---

## 🗺️ Topologia da Rede


![Captura de tela 2025-06-12 114704](https://github.com/user-attachments/assets/0ab85200-4c2e-4694-9b2f-91b8e0b2acce)

---

## 📊 Endereçamento IP

| Descrição da Sub-rede             | Endereço de Rede | Máscara           | Gateway (Agência) |
| :-------------------------------- | :--------------- | :---------------- | :---------------- |
| Agência Goiânia (LAN)             | 10.10.0.0        | 255.255.255.240   | 10.10.0.1         |
| Agência Anápolis (LAN)           | 10.10.0.16       | 255.255.255.240   | 10.10.0.17        |
| Agência Catalão (LAN)            | 10.10.0.32       | 255.255.255.240   | 10.10.0.33        |
| Link Goiânia–Anápolis            | 10.10.0.48       | 255.255.255.240   | N/A               |
| Link Goiânia–Catalão             | 10.10.0.64       | 255.255.255.240   | N/A               |
| Link Anápolis–Catalão            | 10.10.0.80       | 255.255.255.240   | N/A               |
| Rede Internet Simulada (ISP)    | 10.10.0.96       | 255.255.255.240   | N/A               |

---

## ✅ Como Testar a Rede (mesmo sem saber muito de redes)

Para pessoas recrutadoras ou avaliadoras não técnicas, seguem algumas formas simples de testar se a rede está funcionando corretamente dentro do simulador Cisco Packet Tracer:

### 📶 Testar a Conectividade entre Agências
1. Vá até um computador de uma agência (ex: PC1 em Goiânia).
2. Clique nele e vá até a aba **Desktop > Command Prompt**.
3. Digite:
   ```bash
   ping 10.10.0.17
#Teste tambêm:
  ```bash
   ping 10.10.0.33
```
## 🌐 Testar Acesso à Internet Simulada

No mesmo terminal do PC:

bash
Copiar
```bash
ping 8.8.8.8
```
Se a resposta for algo como "Reply from..."
O roteador está fazendo NAT corretamente e o PC está simulando acesso à internet.

## 🧭 Testar as Rotas Estáticas dos Roteadores

Vá até qualquer roteador.
Acesse a aba CLI (linha de comando).

Digite:
```bash
  	show ip route
```
Esse comando exibe todas as rotas configuradas manualmente, que permitem a comunicação entre as redes das agências.

## 📦 Arquivo do projeto

  O arquivo .pkt pode ser aberto diretamente no Cisco Packet Tracer para visualizar e testar a rede.
  ⬇️ [Clique aqui para baixar o projeto Cisco Packet Tracer (.pkt)](https://github.com/devverissimo/Rede_AgenciaBancaria/blob/main/Infra_AgenciaBancaria.pkt)_


  

