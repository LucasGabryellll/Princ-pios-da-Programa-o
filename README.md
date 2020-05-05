# Princípios

# DRY

Don't Repeat Youself.
"Não se repita".

ERRADO: Não repetir código.
CERTO: Não repetir regra de negócio.

## Exemplo: 

- Otimização prematura!

### Front-end

<Table columns={[NOME]} data={[]} parseData={(columns => column.name == 'Nome')} sort />

### Back-end

users {
    name
    email
    password
}

CrudController (index, show, create, update, delete):

- Automaticamente implementa todos os métodos e os outros so herdam esses métodos.

# KISS

keep is simple and stupid.
"Mantenha o Código simples e estúpido".

- Códificar algo que qualquer um entenda!

## Exemplo:

- Colocar coisas difíceis de entender. 

- ERRADO:

```js
function showUserInformation(data) {
    return data.map(u => ({
        name: u.name,
        age: u.age,
    }))
}
```
- CERTO:

```js
function showUserInformation(users) {
    return data.map(user => ({
        name: user.name,
        age: user.age,
    }))
}
```

# YAGNI

You ain't gonna need it.
"Você não irá precisar disso".