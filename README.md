# PetMania API

## 1. Sobre o projeto

O **PetMania** é um sistema desenvolvido para o gerenciamento de animais de estimação, permitindo cadastrar, visualizar e excluir pets por meio de uma API integrada a uma interface Web.

O projeto tem como objetivo demonstrar o funcionamento de uma aplicação que utiliza operações HTTP para realizar o gerenciamento de informações, garantindo a comunicação entre o Front-end e o Back-end.

Nesta atividade, foi realizada a correção da API PetMania, seguida de testes para verificar o funcionamento das funcionalidades disponíveis. Os testes foram executados de duas maneiras: utilizando o Postman, para validar diretamente as requisições à API, e utilizando a interface Web, para verificar o funcionamento das operações na aplicação.

## 2. Objetivos da atividade

- Corrigir problemas de funcionamento da API PetMania.
- Verificar a comunicação entre o Front-end e o Back-end.
- Testar as operações HTTP disponibilizadas pela API.
- Realizar requisições utilizando o Postman.
- Validar as funcionalidades diretamente pela interface Web.
- Conferir se os dados cadastrados e excluídos são atualizados corretamente.

## 3. Tecnologias e ferramentas utilizadas

- **API REST:** responsável pelo processamento das requisições e gerenciamento dos dados dos animais.
- **Postman:** ferramenta utilizada para realizar requisições HTTP e verificar as respostas da API.
- **Interface Web:** utilizada para testar as funcionalidades de maneira visual e interativa.
- **JSON:** formato utilizado para envio e recebimento de dados nas requisições da API.
- **Localhost:** ambiente local utilizado durante a execução e os testes da aplicação.

## 4. Funcionalidades testadas

Durante a atividade, foram verificadas as seguintes funcionalidades:

| Funcionalidade | Método HTTP | Descrição |
|---|---|---|
| Listar pets | GET | Retorna os animais cadastrados. |
| Cadastrar pet | POST | Adiciona um novo animal ao sistema. |
| Excluir pet | DELETE | Remove um animal cadastrado. |

## 5. Testes realizados com Postman

O Postman foi utilizado para testar diretamente os endpoints da API, permitindo verificar o envio das requisições e os retornos recebidos.

### 5.1. GET – Listagem de pets

Foi realizada uma requisição GET para consultar os animais cadastrados.

**Endpoint:**

`http://localhost:8080/api/pets`

**Resultado esperado:**

A API deve retornar uma lista contendo os animais cadastrados, apresentando informações como:

- ID;
- Nome;
- Espécie;
- Raça;
- Idade;
- Sexo;
- Porte;
- Personalidade;
- Disponibilidade para adoção;
- URL da foto.

**Resultado obtido:**

A requisição retornou o status HTTP 200 (OK), demonstrando que a consulta foi realizada com sucesso. Entre os registros retornados estava o pet Pingo, identificado pelo ID 2.

### 5.2. POST – Cadastro de pet

Foi realizada uma requisição POST para cadastrar um novo animal.

**Endpoint:**

`http://localhost:8080/api/pets`

**Exemplo de dados enviados:**

```json
{
  "disponivel": true,
  "especie": "Gato",
  "foto": "https://images.unsplash.com/photo-...",
  "id": 3,
  "idade": 4,
  "nome": "Mida",
  "personalidade": "teste",
  "porte": "Pequeno",
  "raca": "Branco",
  "sexo": "Fêmea"
}
```

**Resultado esperado:**

A API deve receber os dados enviados e realizar o cadastro do novo animal.

**Resultado obtido:**

A requisição retornou o status HTTP 200 (OK), indicando que a operação foi processada com sucesso. O cadastro de Mida foi realizado e o registro passou a aparecer na visualização da aplicação.

### 5.3. DELETE – Exclusão de pet

Foi realizada uma requisição DELETE para remover um animal cadastrado.

**Endpoint:**

`http://localhost:8080/api/pets/2`

**Resultado esperado:**

A API deve localizar o animal pelo seu identificador e realizar sua exclusão.

**Resultado obtido:**

A requisição retornou o status HTTP 200 (OK), acompanhada da mensagem:

`Pet deletado com sucesso!`

Isso demonstrou que a operação de exclusão foi executada corretamente.

## 6. Testes realizados na interface Web

Além dos testes realizados diretamente na API, também foram verificadas as funcionalidades por meio da interface Web do PetMania.

A interface permite que o usuário interaja com o sistema sem precisar realizar manualmente as requisições HTTP.

### 6.1. Visualização inicial

Ao acessar a aplicação, foi possível visualizar a página inicial do PetMania, contendo a apresentação do sistema e a seção destinada aos animais cadastrados.

Inicialmente, a aplicação apresentou a mensagem de que nenhum pet estava cadastrado.

### 6.2. Cadastro de pet pela Web

Foi utilizado o botão de cadastro para abrir o formulário de inclusão de um novo animal.

O formulário disponibiliza os seguintes campos:

- Nome do pet;
- Espécie;
- Raça;
- Idade;
- Sexo;
- Porte;
- Personalidade;
- URL da foto;
- Disponibilidade para adoção.

Após preencher os campos, foi possível salvar o cadastro e verificar sua inclusão na página principal.

O animal cadastrado passou a ser exibido em um cartão com suas respectivas informações.

### 6.3. Exclusão de pet pela Web

Também foi testada a funcionalidade de exclusão diretamente pela interface.

Ao selecionar a opção de excluir um animal, o sistema apresentou uma caixa de confirmação, perguntando se o usuário realmente desejava realizar a operação.

Após confirmar a exclusão, a aplicação apresentou a mensagem:

`Pet excluído com sucesso!`

O animal removido deixou de aparecer na listagem, demonstrando que a interface estava integrada à API e que a operação foi concluída corretamente.

## 7. Resultados dos testes

Após a realização dos testes, foi possível verificar o funcionamento das principais operações da API tanto pelo Postman quanto pela interface Web.

| Teste | Postman | Interface Web |
|---|---|---|
| Listar pets | Sucesso | Sucesso |
| Cadastrar pet | Sucesso | Sucesso |
| Excluir pet | Sucesso | Sucesso |

Os resultados demonstraram que as operações de consulta, cadastro e exclusão estavam funcionando conforme esperado durante os testes realizados.

Também foi possível verificar que as alterações feitas por meio da interface Web eram refletidas na listagem dos animais, evidenciando a comunicação entre as duas partes da aplicação.

## 8. Conclusão

A atividade de correção e testes da API PetMania permitiu colocar em prática os conhecimentos relacionados ao desenvolvimento de APIs REST, aos métodos HTTP e à integração entre Front-end e Back-end.

Com a utilização do Postman, foi possível testar individualmente as requisições e verificar os códigos de resposta retornados pela API. Já os testes realizados na interface Web permitiram validar o funcionamento das mesmas operações de uma perspectiva mais próxima da experiência do usuário.

Ao final da atividade, as funcionalidades de listagem, cadastro e exclusão de animais foram testadas com sucesso nas duas formas de utilização.

Dessa maneira, a atividade contribuiu para compreender a importância dos testes no desenvolvimento de software, principalmente para garantir que uma API funcione corretamente tanto de maneira independente quanto integrada a uma aplicação Web.

## 9. Evidências dos testes

As evidências da execução das operações estão organizadas no documento de testes **Pet Mania - Test by Postman and Web.pdf**, contendo registros visuais das requisições realizadas no Postman e das funcionalidades executadas na interface Web.

As imagens demonstram:

- Requisição GET realizada pelo Postman.
- Requisição POST realizada pelo Postman.
- Requisição DELETE realizada pelo Postman.
- Interface inicial do PetMania.
- Formulário de cadastro de animais.
- Exibição dos animais cadastrados.
- Confirmação e conclusão da exclusão de um animal.

---

**Projeto:** PetMania  
**Atividade:** Correção e testes de API  
**Ambiente de testes:** Localhost  
**Ferramentas de teste:** Postman e navegador Web
