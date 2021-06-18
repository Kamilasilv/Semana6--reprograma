## Semana 6- Introdução API 🚀
Nesta semana vimos alguns conceitos iniciais sobre APIs, metodos HTTP, requisições, JSON, API REST e API RESTfull. A atividade proposta foi a pesquisa acerca de alguns conceitos e alguns casos para imprimir no console.


### **1) Qual a relação entre os métodos HTTP e o CRUD?**
Os Métodos HTTP são espécies de requisições que podemos fazer e são  responsáveis por indicar uma ação a ser feita sobre determinado recurso. Existem vários tipos de métodos HTTP: GET, HEAD, POST, PUT, PATCH, DELETE, TRACE. Já o CRUD é o nome dado a uma funcionalidade que um sistema de banco de dados pode executar, que trabalha com apenas 4 elementos:  Create,Read,Update e Delete. Que são similares a algumas funções feitas por metodos https. Criar, ler as informações, atualizar e deletar. 

### **2) Comente, com exemplos, a diferença entre o PUT e o PATCH.**
 O PATCH é utilizado quando se quer atualizar partes de um recurso.

Exemplo: 

('/aluna/123') 
resultado : {aluna-123}
 
  Já o PUT, atua de maneira diferente por alterar todo o recurso.Podendo ser utilizado para atualizar todo aquele recurso existente ou criar um novo, caso não exista.
  
Exemplo: 

('/aluna/123')
 resultado: {nome: leticia, id: 123, turma: back-end}

### **3) Assim como na aula, apresente os dados dos JSONs no console.**
- No colors-rgb.js apresente o nome da cor e o codigo RGB como no exemplo: "gainsboro - rgb(220, 220, 220, 1)"

        let cores = obj[0]
        for (let prop in cores){
            console.log(` ${prop} -rgb ( ${cores[prop]} )`)
        }

- No estados-cidade.js apresente o nome do Estado, a sigla e todas as cidadades, sem arrays aparentes no console.

        let pais = data[0]
        let estados = pais.estados

        estados.forEach(estados => {
            console.log(`\n Nome do estado: ${estados.nome} , Sigla: ${estados.sigla}, Cidades: `)
        estados.cidades.forEach(cidade => {
            console.log(` ${cidade}`)
            });
        });

- No filmes.js apresente titulo, plot, generos e lingua. Genero e lingua devem ser apresentados em arrays no console.

        let Genre = []
        let Language = []

        for (let i=0; i< obj.length; i++){
        let filme = obj[i]
        console.log('TÍTULO:', filme.Title)
        console.log('PLOT:', filme.Plot)
        let genero = [filme.Genre]
        let language = [filme.Language]
        console.log("GÊNERO" ,genero)
        console.log("LINGUGAGEM" ,language, "\n")
        }

### **4) Defina o conceito de idempotência e como uma API pode ser idempotente**

 IDEMPOTÊNCIA, termo utilizado a métodos que podem ser chamados diversas vezes sem acarretar problemas. Para uma API ser indempotente ela precisa utilizar os métodos de indempotência HTTP, para que mesmo um termo aplicado por varias vezes intencionalmente ou não, ele não prejudicará o sistema. Tendo uma API REST indepomtente. Exemplo disso é quando se requisita o método GET em um servidor, ele irá apenas retornar os dados a cada uso, a cada vez que for chamado. Não irá alterar algo que exista no servidor caso seja requisitado.
        GET, OPTIONS, HEAD, PUT, TRACE, CONNECT e DELETE são idempotentes.
        POST E PATCH não são idempotentes.

### **5) Cite alguns diferentes padrões de projetos de software.**

Padrões de projetos ou "Design patterns" são soluções para problemas comuns que são encontrados no desenvolvimento ou manutenção de um software orientado a objetos. As abstrações que surgem durante um projeto são as chaves para torná-lo flexível. Os padrões de projeto ajudam a identificar abstrações menos óbvias bem como os objetos que podem capturá-las. GoF Patterns (Padrões GoF). Os padrões GoF foram divididos e categorizados de acordo com a natureza do problema que eles resolvem ou tentam resolver.
    Padroes criacionais;
    Padrões estruturais;
    Padrões comportamentais. 

### Referências: 

**Métodos de requisição HTTP** disponível em :<https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods>

**PATCH** disponível em: <https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/PATCH>

**Tutorial da API REST** <https://restfulapi.net/idempotent-rest-apis/>

**Conheça os Padrões de Projeto** disponível em : <https://www.devmedia.com.br/conheca-os-padroes-de-projeto/957>

**CRUD: o que é este conceito no Desenvolvimento de Sistemas** disponível em: <https://angelopublio.com.br/blog/crud>


