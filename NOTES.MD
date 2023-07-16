# NOTES

## Adding environment local to netlify

```sh
pnpm add --global netlify-cli
netlify login
netlify link
netlify env:import .env
```

## Install Prisma

```sh
pnpm add --global prisma
pnpm add -D @prisma/client
prisma generate
prisma migrate dev
prisma migrate reset
```
