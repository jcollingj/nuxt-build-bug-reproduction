To reproduce bug:
- Clone repo
- Install with `npm install`
- Add a Nuxt UI Pro key otherwise that will error during the build
- Run `npx nuxi build`

To run build without bug:
Comment out `'@nuxthq/studio'` in `nuxt.config.ts`