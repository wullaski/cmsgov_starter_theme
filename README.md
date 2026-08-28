# CMSGOV starterkit theme

Generated from starterkit_theme. Additional information on generating themes can be found in the [Starterkit documentation](https://www.drupal.org/docs/core-modules-and-themes/core-themes/starterkit-theme).


## CMS Design System assets

This theme uses the [@cmsgov/design-system](https://design.cms.gov/) package. Its compiled CSS, fonts, and web-component bundle are copied from `node_modules` into `assets/cmsds/`, which is **git-ignored** and not committed.

Because the vendored assets are not in git, you must generate them:

```bash
yarn install
yarn vendor:cmsds
```

Run `yarn vendor:cmsds` in these situations:

- **Initial setup** — after cloning the repo and running `yarn install`.
- **After a version bump** — whenever `@cmsgov/design-system` is updated in `package.json` / `yarn.lock`.
- **In CI/CD** — as a build step after `yarn install`, before deploying the theme.

There is intentionally no `postinstall` hook (auto-run install scripts can be flagged by security scanners), so the command must be run manually.