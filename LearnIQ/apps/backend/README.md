# backend

To install dependencies:

```bash
bun install
```

## Configuration

Set `DATABASE_URL` to your PostgreSQL connection string in `apps/backend/.env`, then apply the Prisma schema from `apps/backend`:

```bash
bunx prisma db push
```

Set `GEMINI_API_KEY` in the same file to enable Gemini-powered interview responses.

To run:

```bash
bun run start
```

This project was created using `bun init` in bun v1.3.14. [Bun](https://bun.com) is a fast all-in-one JavaScript runtime.
