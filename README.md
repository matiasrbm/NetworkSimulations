# NetworkSimulations

Bem-vindo ao repositório **NetworkSimulations**! Este repositório contém projetos pessoais de simulações de redes desenvolvidos utilizando ferramentas como **Cisco Packet Tracer** e **EVE-NG**. O objetivo é explorar, testar e documentar configurações de rede, topologias e cenários práticos para aprendizado e experimentação.

## Sobre o Repositório

Aqui você encontrará simulações de rede que abrangem diferentes conceitos, como:
- Configuração de roteadores e switches.
- Implementação de protocolos de roteamento (OSPF, BGP, RIP, etc.).
- Configuração de VLANs, NAT, ACLs e VPNs.
- Simulações de redes corporativas, data centers e cenários de segurança.
- Testes de desempenho e troubleshoot em ambientes virtuais.

🔧 Este repositório está em constante evolução.


# Projeto 01 - Topologia Corporativa com HSRP, VLANs e Redundância

Este projeto simula uma infraestrutura de rede corporativa utilizando o **Cisco Packet Tracer**, inspirado nos conceitos e práticas do curso **"Redes de Computadores Básico Mão na Massa"** do professor Gustavo Kalau.

## Tecnologias e Protocolos Utilizados

- Cisco Packet Tracer
- HSRP (Hot Standby Router Protocol)
- VLANs e Trunking
- Spanning Tree Protocol (STP)
- DHCP
- NAT
- ACLs
- Redundância de links com dois ISPs (BATATA e BROCOLIS)

## Descrição da Topologia

- **CORE1**: Root STP, Gateway principal e master no HSRP
- **CORE2**: Backup HSRP com comunicação redundante com os access switches
- **Servidores**:
  - Servidor DHCP
  - Servidor Web
  - Ambos alocados na VLAN 400 (10.0.0.0/24)
- **VLANs de Acesso**:
  - VLAN 100 - Financeiro (172.16.0.0/24)
  - VLAN 200 - RH (172.16.10.0/24)
  - VLAN 300 - Diretoria (172.16.20.0/24)
- **Switches de Acesso (AC1 a AC4)** com estações de trabalho
- **Dois ISPs (BATATA e BROCOLIS)** conectando à Internet (via 8.8.8.8)

## Objetivos do Projeto

- Criar redundância na camada de distribuição com HSRP
- Segmentar a rede com VLANs para maior organização e segurança
- Utilizar STP para evitar loops de rede
- Garantir acesso externo via dois provedores com failover
- Simular serviços reais (DHCP e Web)
- Controlar o tráfego com ACLs
