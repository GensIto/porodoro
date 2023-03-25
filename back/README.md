# Project

初回パッケージインストール
nest prisma sqlite

```
nest new // backののち
yarn add @nestjs/core @nestjs/common @nestjs/platform-express @nestjs/cli prisma sqlite3

```

### Prisma

初回パッケージインストール後

```
npx prisma init
touch database.sqlite
```

prisma/schema.prisma ファイルを編集し、SQLite を使用するように変更します。以下のように変更します。

```
datasource db {
  provider = "sqlite"
  url      = "file:./database.sqlite"
}
```

```
nest g service prisma --no-spec
nest g module prisma --no-spec
```

app に import する
