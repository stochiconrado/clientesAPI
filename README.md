# clientesAPI

## API de CRUD do Sujeito Programador

- Parte 1: [Backend](https://youtu.be/XuTfN_84rcU)
- Parte 2: [Frontend](https://youtu.be/JlYrbEBZ3PE)

### Backend

- **NodeJS**: [NodeJS](https://nodejs.org/dist/v20.9.0/node-v20.9.0-linux-x64.tar.xz)

`npm init -y`

- **TypeScript**: TypeScript é uma linguagem de programação de código aberto desenvolvida pela Microsoft. É um superconjunto sintático estrito de JavaScript e adiciona tipagem estática opcional à linguagem.
  
Adicione o TypeScript no projeto, em ambiente de desenvolvimento, permitindo mais segurança para o projeto:

`npm install @types/node --save-dev`

Inicialize o projeto depois de instalar typescript

`tsc --init`

- **Prisma**: ORM utilizando no projeto como uma forma de interligar MongoDB com TypeScript.

Adicione o Prisma CLI como dependênncia de desenvolvimento no projeto
  
`npm install prisma --save-dev`

Instale o cliente do prisma

`npm install @prisma/client`

Gerando esquema da base de dados utilizado pelo Prisma.

`npx prisma generate`

Inicializando esquema da base de dados do prisma.

`npx prisma init`

Altere o provedor de banco de dados do default para mongodb no arquivo prisma/schema.prisma

>datasource db {
>
>provider = "mongodb"
>
>url      = env("DATABASE_URL")}

Instale o Prisma Studio para visualizar a base de dados.
`npx prisma studio`

**MongoDB**: MongoDB é um software de banco de dados orientado a documentos livre, de código aberto e multiplataforma, escrito na linguagem C++. Classificado como um programa de banco de dados NoSQL, o MongoDB usa documentos semelhantes a JSON com esquemas. É desenvolvido pela MongoDB Inc. e publicado sob uma combinação da GNU Affero General Public License e Licença Apache. Suas características permitem com que as aplicações modelem informações de modo muito mais natural, pois os dados podem ser aninhados em hierarquias complexas e continuar a ser indexáveis e fáceis de buscar.

Conecte o MongoDB com o projeto através do DATABASE_URL gerado com o MongoDB, ao iniciar um novo cluster.
DATABASE_URL é encontrado no arquivo .env na raíz do projeto.

## Frontend

**ReactJS**: React faz com que a criação de UIs interativas seja uma tarefa fácil. Crie views simples para cada estado na sua aplicação, e o React irá atualizar e renderizar de forma eficiente apenas os componentes necessários na medida em que os dados mudam. Views declarativas fazem com que seu código seja mais previsível e simples de depurar.

**Vite**: Vite (palavra francesa para "rápido", pronunciado /vit/, como "veet") é uma ferramenta de construção que visa fornecer uma experiência de desenvolvimento mais rápida e enxuta para projetos web modernos. Consiste em duas partes principais:

- Um servidor de desenvolvimento que fornece aprimoramentos avançados de recursos em relação aos módulos ES nativos, por exemplo, Hot Module Replacement (HMR) extremamente rápido.

- Um comando de construção que agrupa seu código com Rollup, pré-configurado para gerar ativos estáticos altamente otimizados para produção.

Vite também é altamente extensível por meio de sua API de plug-in e API JavaScript com suporte completo para digitação.

Crie um projeto com Vite, nomeando o projeto e escolhendo um framework JavaScript, no caso React, e tipo de estrutura, Typescript.

`npm create vite@latest <nomedoprojeto>`

**TailwindCSS**: Tailwind CSS funciona verificando todos os seus arquivos HTML, componentes JavaScript e quaisquer outros modelos em busca de nomes de classes, gerando os estilos correspondentes e, em seguida, gravando-os em um arquivo CSS estático.

É rápido, flexível e confiável — com tempo de execução zero.

Instale o TailwindCSS no projeto, PostCSS

` npm install -D tailwindcss postcss autoprefixer `

Inicialize o TailwindCSS

`npx tailwindcss init`

Configure template de diretórios

>/** @type {import('tailwindcss').Config} */
>
>module.exports = {
>
>content: ["./src/**/*.{html,js}"],
>
>theme: {
>
>extend: {},
>
>},
>
>plugins: [],
>
>}

Em `src/input.css` adcione as diretivas utilizadas pelo TailwindCSS para um melhor funcionamento da ferrammenta

>@tailwind base;
>
>@tailwind components;
>
>@tailwind utilities;

No terminal start o Tailwind CLI

`npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`

### Finalizando

#### Faça tudo isso depois de clonar o repositório e tenha uma aplicação que cadastra, lista e deleta. Podendo ser utlizado em diversas aplicações
