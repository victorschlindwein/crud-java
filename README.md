# crud-java-rh-api

Projeto simples de um CRUD em Java usando o Spring.
  
Método de execução: Após baixar e buildar o projeto ele ficará disponível no localhost:8080

As rotas disponíveis estão documentadas abaixo.

## GET: /funcionarios. 
Método retorna os cadastros de funcionários realizados na API.   
Exemplo de retorno vazio.   
`Statuscode: 200`.
```
[]
```

## POST: /funcionarios.
Método insere um dado do tipo funcionário novo dentro do banco de dados da aplicação (JPA).  
Exemplo:   
Dados enviados:
``` 
{
    "nome": "Funcionario Teste",
    "email": "funcionarioteste@teste.com",
    "salario": 6000,
    "dataAdmissao": "2023-06-21",
    "status": "ATIVO"
}
```

Dados Recebidos `Statuscode: 201`:
``` 
{
    "id": 1,
    "nome": "Funcionario Teste",
    "email": "funcionarioteste@teste.com",
    "salario": 6000,
    "dataAdmissao": "2023-06-21",
    "status": "ATIVO"
}
```

## GET: /funcionarios/{id}
Método retorna o cadastro de um funcionário específico da API.  
Exemplo de resposta `statuscode 200` para o id 1.
```
{
    "id": 1,
    "nome": "Funcionario Teste",
    "email": "funcionarioteste@teste.com",
    "salario": 6000,
    "dataAdmissao": "2023-06-21",
    "status": "ATIVO"
}
```

## PUT: /funcionarios/{id}. 
Método modifica alguma informação no funcionário com id enviado na requisição.  
O body deve conter um objeto do tipo funcionário modificado.  
Exemplo de envio:
```
{
    "id": 1,
    "nome": "Funcionario Teste Modificado",
    "email": "funcionario_teste@teste.com",
    "salario": 8000,
    "dataAdmissao": "2023-06-21",
    "status": "ATIVO"
}
```

Exemplo de retorno: `statuscode 200`
```
{
    "id": 1,
    "nome": "Funcionario Teste Modificado",
    "email": "funcionario_teste@teste.com",
    "salario": 8000,
    "dataAdmissao": "2023-06-21",
    "status": "ATIVO"
}
```
