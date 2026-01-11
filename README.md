# The Problem

- Setup the project and run the dev server you'll see this error

```bash
Error: [vite-env-only] Import denied
 - Denied by specifier pattern: /^node:/
 - Importer: index.html
 - Import: "node:fs"
 - Environment: client
```

- With the `vite-env-plugin` plugin used and enabled in the `vite.config.ts` file
- This plugin detects unknown imports of `node:fs` in an unknown file, `index.html`

# This problem is not related to Intlayer

I think the main issue is that the plugin is too old and is no longer maintained for newer versions of Remix.js and ReactRouter.

# A Solution ?

- Remove the plugin and trust your Intuition to not import server modules into client files :-)

