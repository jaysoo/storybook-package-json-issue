This is a repro of `package.json` being created in a monorepo unexpectedly.

```shell
pnpm i
cd apps/demo
npx storybook dev
```

Observe that `apps/demo/package.json` is now created with the following:

```json
{
  "name": "demo",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

This was not the case with `storybook@7.5.3`, and first started happening in `storybook@7.6.0`.
