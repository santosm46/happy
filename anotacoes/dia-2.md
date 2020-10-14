

## Iniciando

### Cria o package.json
- `yarn init -y`

### Adicionando express
- `yarn add express`
- `yarn add @types/express -D`

### Adicionar typescript
- `yarn add typescript -D`
- `yarn tsc --init`

isso cria o tsconfig.json, mudar
- "target":"es2017"

### Executar projeto
- `yarn add ts-node-dev -D`

depois adicionar "scripts" no package.json

### Banco de dados

- `yarn add typeorm sqlite3`

ORM = Object Relational Mapping

criar arquivos em src/database e ormconfig.json

criar e editar arquivo da migration
- `yarn typeorm migration:create -n create_orphanages`
- `yarn typeorm migration:run`

reverter ação
- `yarn typeorm migration:revert`


usar beekeeper studio para visualizar os dados

criar pasta src/models<br>
setar `"strictPropertyInitialization": false` em tsconfig.json<br>
desmarcar opções "experimentalDecorators" e "emitDecoratorMetadata"


### Lidar com imagens
criar tabela para armazenar imagens
- `yarn typeorm migration:create -n create_images`
- `yarn typeorm migration:run`

- `yarn add multer`
- `yarn add @types/multer -D`

### Lidar com erros
- `yarn add express-async-errors`<br>

adicionar `import 'express-async-errors';` em server.ts<br>
criar pasta src/errors

### Validação
- `yarn add yup`
- `yarn add @types/yup -D`
adicionar código para validação em OrphanagesController.ts


### Por fim...
Para permitir ter requisições de apps em outras portas
- `yarn add cors`
- `yarn add @types/cors -D`