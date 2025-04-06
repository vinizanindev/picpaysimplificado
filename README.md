# <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/PicPay_Logogrande.png" width="50"/> PicPay Simplificado

Este projeto é uma API RESTful que simula um sistema de transferências entre usuários, inspirada no funcionamento de plataformas como o PicPay. Ele foi desenvolvido como parte de um desafio técnico para avaliação de conhecimentos em back-end.

## 🚀 Tecnologias utilizadas

- Java 17
- Spring Boot
- JPA (Hibernate)
- H2 Database (em memória)
- Maven
- REST Template (para integração com APIs externas)
- Lombok

## 📌 Requisitos atendidos

✔️ Cadastro de usuários com validações de unicidade (CPF e e-mail)  
✔️ Diferença entre usuários comuns e lojistas  
✔️ Transferência entre usuários com verificação de saldo  
✔️ Lojistas não podem enviar dinheiro, apenas receber  
✔️ Chamada a API externa para autorização da transação  
✔️ Transações revertidas em caso de falha  
✔️ Notificações via mock de API externa  
✔️ Arquitetura em camadas (Controller, Service, Repository, Domain, DTO)  
✔️ Código limpo, organizado e pronto para manutenção  

---

## 📂 Estrutura de pastas

src/ └── main/ └── java/com/picpaysimplificado/ ├── controller/ ├── domain/ ├── dtos/ ├── repositories/ ├── services/ └── resources/ └── application.properties

---

## 🔄 Endpoints disponíveis

### 📤 POST `/transfer`

Realiza uma transferência entre dois usuários.

**Request:**
```json
{
  "value": 100.0,
  "payer": 1,
  "payee": 2
}
{
  "id": 1,
  "amount": 100.0,
  "sender": {...},
  "receiver": {...},
  "timestamp": "2025-04-06T15:00:00"
}
```
# 👤 POST /users
## Cria um novo usuário.
```
{
  "name": "Vinicius Zanin",
  "document": "12345678901",
  "email": "vinicius@email.com",
  "balance": 500.00,
  "userType": "COMMON"
}
```
# ⚙️ Como rodar o projeto
```
# Clone o repositório
git clone https://github.com/seu-usuario/nome-do-repo.git
cd nome-do-repo

# Build do projeto
./mvnw clean install

# Rode a aplicação
./mvnw spring-boot:run

```
# 👨‍💻 Desenvolvedor

**Vinicius Zanin**
[LinkedIn](https://www.linkedin.com/in/viniciuszanin)

# 📝 Observações
API externa para autorização: https://util.devi.tools/api/v2/authorize

API externa para notificações: https://util.devi.tools/api/v1/notify

Banco de dados usado: H2 em memória (para facilitar testes locais)

Este projeto é apenas um desafio técnico e não representa o PicPay oficialmente.
