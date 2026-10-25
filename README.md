# ProFabX website

`web/` contains the built public website: home, quote workbench, CMF, partners and about pages. Relative asset URLs support a GitHub Pages repository subpath.

## Deployment

Configure repository Settings → Pages → Source as GitHub Actions. Pushing the default branch (main or master) or dispatching the Publish ProFabX website workflow publishes only `web/`.

## Public and local capabilities

Model imports, placement, quote calculations, local browser storage, materials and transaction downloads run in the browser. GitHub Pages is a static host: native Bambu/Creality slicing, real-time desktop synchronization and native support generation require the separate local ProFabX preview service. No native executables, user models/orders, login profiles, runtime descriptors or engineering backups are included here.

## Updates

Build the local website with the existing Vite project, then replace `web/` with its `dist/` output while preserving `.nojekyll`. The engineering source and native toolchain remain in the local project.
