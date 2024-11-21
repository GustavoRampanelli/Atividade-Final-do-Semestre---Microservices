# 🌟 Atividade Final do Semestre - Microservices 🌟

Este repositório contém a implementação de uma arquitetura de microservices desenvolvida como atividade final do semestre. A solução foi projetada com integração entre os serviços, balanceamento de carga e orquestração via Docker Compose.

## 🛠 Microserviços

### 🔄 **cambio-service**  
Serviço responsável por operações de câmbio.

### 📦 **produto-service**  
Serviço para gerenciamento de produtos.

### 💬 **saudacao-service**  
Serviço simples de saudação.

### 🛠 **config-service**  
Serviço para configuração centralizada.

### 📡 **eureka-service**  
Serviço de registro e descoberta de microservices.

### 🌐 **api-gateway-service**  
Porta de entrada para os microservices, configurada com rotas e filtros personalizados.

---

## 🌐 **Configuração do API Gateway**

O API Gateway foi configurado com:
- Rotas para **cambio-service**, **produto-service** e **saudacao-service**.
- Filtro de cabeçalho para todas as requisições:
  ```yaml
  filters:
    - AddRequestHeader=Usuario,Seu Nome Completo


## 🐳 **Docker Compose**
O repositório inclui um arquivo compose.yaml com os seguintes serviços configurados:

### Eureka Service
Para registro e descoberta dos microservices.

### Cambio Database (MySQL)
Banco de dados para o serviço de câmbio.

### Cambio Service
Configurado para rodar duas instâncias, garantindo balanceamento de carga.

### Produto Database (MySQL)
Banco de dados para o serviço de produtos.

### Produto Service
Serviço conectado ao banco de produtos.

### API Gateway Service
Porta de entrada para todos os microservices.

## 🚀 Como Executar
### Certifique-se de ter o Docker e o Docker Compose instalados.
### Clone este repositório:
https://github.com/GustavoRampanelli/Atividade-Final-do-Semestre---Microservices
### Acesse a pasta do repositório:
 cd seu-repositorio
### Suba os serviços com:
 docker-compose up
### Acesse os serviços pelos seguintes endereços:
### Eureka Service: http://localhost:8761
### API Gateway: http://localhost:8080


## 🧪 **Teste das Rotas**
### Endpoints Disponíveis:
### Cambio-Service:
### GET http://localhost:8080/cambio/{endpoint}
### Produto-Service:
### GET http://localhost:8080/produto/{endpoint}
### Saudacao-Service:GET http://localhost:8080/saudacao/{endpoint}


