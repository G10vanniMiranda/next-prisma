#### Criando App Nexts / Prisma 5 passo ao sucesso

* 1 Criar o projeto NextJS 15

npx create-next-app@latest app3´


* 2 Instalar o Prisma ORM

npm i prisma


* 3 Iniciar o serviço do Prisma

npx prisma init --datasource-provider sqlite


* 4 Criar os Modelos do Prisma ORM

model Produto{
  id        Int @id @default(autoincrement())
  nome      String @unique
  descricao String 
  preco     Float

  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt

  @@map("produto")
}


* 5 Rodar as migration

npx prisma migrate dev