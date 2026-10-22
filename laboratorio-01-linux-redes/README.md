# Lab 01 — Linux and Networking Fundamentals

## Objective

Este laboratório reúne 25 exercícios introdutórios realizados em Linux, com foco em administração de sistemas, redes de computadores e fundamentos de cibersegurança.

O objetivo é desenvolver familiaridade com o terminal, compreender o funcionamento básico do sistema operacional e aprender a analisar conectividade, processos, permissões e serviços de rede.

## Environment

- Sistema operacional: Ubuntu Linux
- Ambiente de prática: máquina virtual VMware
- Ferramentas: terminal Linux e utilitários de sistema e rede
- Tipo de atividade: laboratório educacional

## Exercise 01 — System Identification

**Comandos utilizados:**

```bash
whoami
hostname
pwd
```

**Objetivo:** identificar o usuário atual, consultar o nome da máquina e verificar o diretório de trabalho.

**Aprendizado:** compreender informações básicas sobre a sessão e o ambiente Linux.

## Exercise 02 — Directory Navigation

**Comandos utilizados:**

```bash
cd /etc
pwd
ls -lah
```

**Objetivo:** navegar entre diretórios e listar arquivos com informações detalhadas.

**Aprendizado:** compreender a estrutura de diretórios do Linux e utilizar comandos de navegação.

## Exercise 03 — Hosts File

**Comando utilizado:**

```bash
cat /etc/hosts
```

**Objetivo:** consultar o arquivo local de configuração de nomes de máquinas.

**Aprendizado:** compreender como o arquivo `hosts` pode associar nomes a endereços IP e participar do processo de resolução de nomes.

## Exercise 04 — Network Interfaces

**Comando utilizado:**

```bash
ip addr
```

**Objetivo:** consultar as interfaces de rede e os endereços configurados.

**Aprendizado:** identificar interfaces, estados operacionais e endereços IPv4 e IPv6.

## Exercise 05 — Routing Table

**Comando utilizado:**

```bash
ip route
```

**Objetivo:** examinar as rotas de rede disponíveis no sistema.

**Aprendizado:** compreender o conceito de roteamento e identificar a função de uma rota padrão.

## Exercise 06 — Local Network Connectivity

**Comando utilizado:**

```bash
ping -c 4 <IP_DO_GATEWAY>
```

**Objetivo:** testar a conectividade com o gateway da rede local.

**Aprendizado:** utilizar o `ping` para observar respostas de conectividade e tempos de resposta.

**Nota:** o endereço foi substituído por um marcador para não publicar detalhes desnecessários da configuração local. O marcador deve ser substituído pelo endereço correto caso o comando seja executado novamente.

## Exercise 07 — Internet Connectivity

**Comando utilizado:**

```bash
ping -c 4 1.1.1.1
```

**Objetivo:** testar a conectividade com um destino externo utilizando um endereço IP.

**Aprendizado:** verificar se há respostas ICMP de um destino externo sem depender diretamente da resolução de um nome de domínio.

## Exercise 08 — DNS Resolution

**Comando utilizado:**

```bash
ping -c 4 google.com
```

**Objetivo:** observar a resolução de um nome de domínio durante um teste de conectividade.

**Aprendizado:** compreender a relação entre nomes de domínio, endereços IP e o funcionamento do DNS.

## Exercise 09 — File Permissions

**Comando utilizado:**

```bash
ls -l /etc/hosts
```

**Objetivo:** consultar metadados de um arquivo.

**Aprendizado:** interpretar informações sobre permissões, proprietário, grupo e tamanho de arquivos.

## Exercise 10 — Directory Permissions

**Comando utilizado:**

```bash
ls -ld /etc
```

**Objetivo:** consultar informações sobre um diretório específico.

**Aprendizado:** compreender como as permissões de diretórios controlam operações como leitura, gravação e acesso.

## Exercise 11 — User Groups

**Comando utilizado:**

```bash
groups
```

**Objetivo:** consultar os grupos associados ao usuário atual.

**Aprendizado:** compreender a função dos grupos no gerenciamento de permissões e acessos no Linux.

## Exercise 12 — User Identity and Permissions

**Comando utilizado:**

```bash
id
```

**Objetivo:** consultar os identificadores do usuário e dos grupos associados à sessão.

**Aprendizado:** compreender os conceitos de UID, GID e associação a grupos.

## Exercise 13 — Logged-in Users

**Comando utilizado:**

```bash
who
```

**Objetivo:** consultar informações sobre sessões de usuários no sistema.

**Aprendizado:** conhecer um recurso básico para observar sessões de usuários conectados.

## Exercise 14 — System Uptime

**Comando utilizado:**

```bash
uptime
```

**Objetivo:** consultar o tempo de funcionamento e informações sobre a carga do sistema.

**Aprendizado:** compreender indicadores básicos que ajudam a avaliar o estado operacional de uma máquina Linux.

## Exercise 15 — Operating System Information

**Comando utilizado:**

```bash
cat /etc/os-release
```

**Objetivo:** consultar informações sobre a distribuição Linux instalada.

**Aprendizado:** identificar dados da distribuição e sua versão, úteis para administração e compatibilidade de software.

## Exercise 16 — Disk Usage

**Comando utilizado:**

```bash
df -h
```

**Objetivo:** consultar o espaço total, utilizado e disponível nos sistemas de arquivos.

**Aprendizado:** monitorar a utilização do armazenamento e interpretar as informações apresentadas em formato legível.

**Observação:** imagens de pacotes Snap montadas como sistemas de arquivos somente de leitura podem aparecer com 100% de utilização. Esse resultado deve ser interpretado de acordo com o tipo de montagem, não necessariamente como falta de espaço no disco principal.

## Exercise 17 — Memory Usage

**Comando utilizado:**

```bash
free -h
```

**Objetivo:** consultar informações sobre memória RAM e swap.

**Aprendizado:** compreender a diferença entre memória livre e memória disponível, considerando também o uso de cache pelo sistema operacional.

## Exercise 18 — Running Processes

**Comando utilizado:**

```bash
ps aux
```

**Objetivo:** listar os processos em execução.

**Aprendizado:** consultar informações como usuário, identificador do processo (PID) e utilização de recursos.

## Exercise 19 — Real-time System Monitoring

**Comando utilizado:**

```bash
top
```

**Objetivo:** acompanhar processos e indicadores do sistema em tempo real.

**Aprendizado:** observar a atividade dos processos e a utilização de recursos. A tecla `q` permite sair da ferramenta.

## Exercise 20 — Listening Network Sockets

**Comando utilizado:**

```bash
ss -tuln
```

**Objetivo:** consultar sockets TCP e UDP e identificar portas em estado de escuta.

**Aprendizado:** compreender como ferramentas de linha de comando auxiliam na investigação de conexões e serviços de rede.

## Exercise 21 — Network Services and Processes

**Comando utilizado:**

```bash
sudo ss -tulpn
```

**Objetivo:** investigar sockets de rede e identificar processos associados quando as permissões permitem.

**Aprendizado:** relacionar portas, protocolos e processos para compreender melhor a atividade de rede do sistema.

**Nota de segurança:** este relatório registra o objetivo e o aprendizado da atividade, sem divulgar uma listagem detalhada dos serviços e processos da máquina virtual.

## Exercise 22 — Network Interface Summary

**Comando utilizado:**

```bash
ip -br addr
```

**Objetivo:** obter uma visão resumida das interfaces de rede.

**Aprendizado:** consultar rapidamente os estados das interfaces e os endereços configurados sem precisar analisar uma saída extensa.

## Exercise 23 — Hostname Identification

**Comando utilizado:**

```bash
hostname
```

**Objetivo:** consultar o nome configurado para o sistema.

**Aprendizado:** reconhecer o nome da máquina como uma informação básica de identificação e administração do ambiente.

## Exercise 24 — External Connectivity Test

**Comando utilizado:**

```bash
ping -c 4 8.8.8.8
```

**Resultado observado:** quatro respostas recebidas, sem perda de pacotes durante a execução registrada.

**Objetivo:** avaliar a conectividade com um destino externo.

**Aprendizado:** interpretar respostas do `ping`, observar tempos de resposta e considerar a perda de pacotes como um dos indicadores de conectividade.

**Limitação:** um teste bem-sucedido representa apenas as condições observadas naquele momento e não garante disponibilidade contínua da rede.

## Exercise 25 — Network Path Investigation

**Comando utilizado:**

```bash
tracepath 8.8.8.8
```

**Resultado observado:** o primeiro salto respondeu, mas os saltos seguintes não forneceram respostas às sondagens.

**Objetivo:** investigar o caminho de rede até um destino externo.

**Aprendizado:** compreender o conceito de saltos de rede e reconhecer que roteadores ou outros equipamentos intermediários podem filtrar ou não responder às sondagens.

**Conclusão técnica:** a ausência de respostas em saltos posteriores não comprova, por si só, uma falha de conectividade. Os resultados precisam ser interpretados em conjunto com outros testes.

## Conclusion

Os 25 exercícios permitiram desenvolver conhecimentos introdutórios sobre:

- Navegação no terminal Linux e estrutura de diretórios
- Identificação do sistema operacional e do usuário
- Permissões, usuários e grupos
- Processos e monitoramento de recursos
- Interfaces de rede e endereçamento IP
- Conectividade e resolução de nomes
- Sockets, portas e serviços de rede
- Rotas e investigação do caminho até um destino

Essas atividades representam uma base inicial para estudos mais aprofundados em administração de sistemas, redes e cibersegurança.

As próximas etapas incluem aprofundar os fundamentos de TCP/IP, estudar análise de tráfego, compreender os mecanismos de segurança do Linux e desenvolver novas práticas em ambientes controlados.

## Responsible Practice

As atividades foram realizadas em um ambiente de laboratório educacional.

Qualquer análise ou teste em sistemas de terceiros deve ocorrer somente com autorização adequada e dentro do escopo permitido.



**Concluído:** 25 exercícios introdutórios de Linux e redes.

Este documento registra os comandos praticados, os objetivos das atividades, os resultados observados que foram documentados e os principais aprendizados.
