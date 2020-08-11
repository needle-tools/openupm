---
ads: true
layout: Home
pageClass: homepage
title: Open Source Unity Package Registry (UPM)
heroText: Open Source Unity Package Registry
actionText: Guide
actionLink: /docs/
features:
- title: Open Source UPM Registry
  details: Hosting community selective open source UPM packages
- title: Continuous Publishing
  details: Package publishing automation based on Git tags
- title: Command-Line Tool
  details: <a href="https://github.com/openupm/openupm-cli">OpenUPM-CLI</a> for 3rd-party UPM registries
noGlobalSocialShare: true
---

### Get Started (by modifying the Package Manifest)

1. In your Unity project folder, go to and open `Packages/manifest.json` with a text editor.

2. Add a scoped registry at the top:
  ```sh
  "scopedRegistries": [
    {
      "name": "OpenUPM",
      "url": "https://package.openupm.com",
      "scopes": [
        "com.littlebigfun.addressable-importer"
      ]
    }
  ],
  "dependencies": {
  ```
   You can close `manifest.json` now.
  
3. Back in Unity, open Package Manager.

   Many packages on OpenUPM are in a "preview" state. To use any of them,
    - before 2020.1: make sure to enable `Advanced > Show Preview Packages`
    - 2020.1+: make sure to enable `Project Settings > Package Manager > Enable Preview Packages`
  
4. Find & Install the package in PackMan
    - select "My Registries" in the Registry Dropdown
    - select `Unity Addressable Importer`
    - click Install.

### Get Started (using OpenUPM Command Line Helper)

Make sure you have nodejs / npm installed.

```sh
# Install openupm-cli
$ npm install -g openupm-cli
# OR yarn global add openupm-cli

# Enter your unity project folder
$ cd YOUR_UNITY_PROJECT_FOLDER

# Search a package
$ openupm search addressable-importer
┌───────────────────────────────────────┬─────────┬───────────┬────────────┐
│ Name                                  │ Version │ Author    │ Date       │
├───────────────────────────────────────┼─────────┼───────────┼────────────┤
│ com.littlebigfun.addressable-importer │ 0.4.1   │ Favo Yang │ 2019-11-25 │
│ Unity Addressable Importer            │         │           │            │
└───────────────────────────────────────┴─────────┴───────────┴────────────┘

# Install package
$ openupm add com.littlebigfun.addressable-importer
added: com.littlebigfun.addressable-importer@0.4.1
manifest updated, please open unity project to apply changes
```

::: warning COMPATIBILITY NOTE
openupm-cli requires [Node.js 12](https://nodejs.org/en/)
:::

<ClientOnly><PackageRecent /></ClientOnly>

<social-share />

<style lang="stylus">
</style>
