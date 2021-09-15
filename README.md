### Teste C#

Esta avaliação tem o objetivo de conhecer um pouco do seu conhecimento em Api RESTful/C#.

Recomendamos que você conclua o teste entre 4 - 6 horas.

### Tarefas

Com a seguinte representação de beneficiário:

```json
{
    "nome": "Antônio de Souza Silva",
    "cpf": "25141304094",
	"carteiras": [
		{
			"numero": "970166812",
			"validade": "2023-01-12"
		},
		{
			"numero": "970091589",
			"validade": "2021-02-11"
		}
	],
    "ativo": true
}
```

Crie endpoints para as seguintes ações:

- [ ] Criação de beneficiário onde o payload será o json informado acima (exceto a propriedade **ativo**).

- [ ] Edição de beneficiário por **cpf**.

- [ ] Recuperação de beneficiário por **cpf**.

- [ ] Exclusão de beneficiário por **cpf**.

### Requisitos

- [ ] Toda vez que um beneficiário for recuperado por **cpf**, deverá ser tratada a propriedade **ativo**.

        Um beneficiário é considerado ativo sempre que tiver uma carteira válida.

- [ ] Caso um beneficiário tente ser criado com um **cpf** já existente, uma mensagem deve ser lançada.

        Dois beneficiários são considerados iguais se os seus cpfs forem iguais.

- [ ] Caso um beneficiário tente ser criado com uma **carteira** já existente em outro **cpf**, uma mensagem deve ser lançada.

        Dois beneficiários não podem possuir um mesmo número de **carteira**.

- [ ] Ao atualizar um beneficiário, o antigo deve ser sobrescrito com o que está sendo enviado na requisição.

        A requisição deve receber o cpf e atualizar com o beneficiário que também esta vindo na requisição.

### Dica

- Os beneficiários podem ficar em memória, não é necessário persistir os dados.

### O que valorizamos?

- Boas práticas em RESTful
- Design Patterns
- Testes são bem vindos
