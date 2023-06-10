# Installation
Install Mighty Apps Builder, its dependencies, and complete necessary setup.

## Dependencies
- Node.js 14.17.5 or later (See supported versions [here](https://github.com/mightyapps-org/builder/blob/master/SECURITY.md))
- ReNative version [...] or later (Check installed version with ```rnv --version```) To install ReNative, run:
    ```bash npm2yarn
    $ npm install rnv -g
    ```
:::danger
A known issue involves `create-next-app` not functioning properly in Windows Powershell. For now, it might be best to [use `Windows Subsystem for Linux`](https://learn.microsoft.com/en-us/windows/wsl/install).
:::

## Quick Start Installation
We recommend that you use `create-mighty-app` to set-up a new Mighty Apps Builder application. To create a project, run:
```bash npm2yarn
npm install @docusaurus/remark-plugin-npm2yarn
```

You will be prompted with set-up questions that you must answer:
```bash showLineNumbers
? Enter the name of your project: my-mighty-app
? Enter the title of your project: My Mighty App
? Enter the App ID of your project: com.mycompany.my-mighty-app
? Use a default template app for your project? Yes
```

You should see the following message if the set-up was successful:
```bash
Creating a new Mighty Apps builder project in my-mighty-app
```

## Manual Installation
To install Mighty Apps Builder manually or in an existing application, run the following commands:

:::info

Ensure that the correct version of ReNative listed above is installed.
:::

### Create ReNative project
 
:::caution

  Running `rnv new` directly will not install the latest version of ReNative. Use `npx` (recommended).
:::

   
<Tabs
  defaultValue="rnv"
  values={[
    {label: 'Global RNV', value: 'rnv'},
    {label: 'Using NPX', value: 'npx'},
  ]}>
  <TabItem value="rnv">

  ```bash title=">_ Terminal"
  rnv new
  ```

</TabItem>
<TabItem value="npx">
<Tabs
  defaultValue="npm"
  values={[
    {label: 'Default NPX', value: 'npm'},
    {label: 'NPX with Yarn', value: 'yarn'},
  ]}>
  <TabItem value="npm">

  ```bash title=">_ Terminal"
  npx rnv new
  ```
  </TabItem>
  <TabItem value="yarn">

  ```bash title=">_ Terminal"
  npx rnv new --yarn
  ```

  </TabItem>

</Tabs>
</TabItem>
</Tabs>


Follow the RNV set-up steps to create a new project:
<!-- ```bash
? What's your project Name? (no spaces, folder based on ID will be 
created in this directory) my-mighty-app
? What's your project Title? My Mighty App
? What's your App ID? com.mycompany.my-mighty-app
? What's your Version? 0.1.0
? What workspace to use? rnv
[ task ] [new] loadPluginTemplates[2]
[ task ] [new] _parsePluginTemplateDependencies[2] scope:root      
[ task ] [new] parseRenativeConfigs[2]
[ task ] [new] getWorkspaceDirPath[2]
? What template to use? @rnv/template-starter - Multiplatform starter kit
✔ Executing: npm view @rnv/template-starter versions
✔ Executing: npm dist-tag ls @rnv/template-starter
? What @rnv/template-starter version to use? 0.36.1 (HEAD: latest)
``` -->

```bash
? What's your project Name? (no spaces, folder based on ID will be created in this directory) my-mighty-app
? What's your project Title? My Mighty App
? What's your App ID? com.mycompany.my-mighty-app
? What's your Version? 0.1.0
? What workspace to use? rnv

? What template to use? @rnv/template-starter - Multiplatform starter kit
? What @rnv/template-starter version to use? 0.36.1 (HEAD: latest)
? What platforms would you like to use? ios, android, androidtv, firetv, androidwear, web, webtv, tizen, tvos, webos, macos, windows, tizenwatch, tizenmobile, kaios, firefoxos, firefoxtv, chromecast, xbox

? Do you want to set-up git in your new project? No
┌──────────────────────────────────────────────────────────────────────────────┐
│  🚀  ReNative Project Generator                                              │
│                                                                              │
├──────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Project Name (folder): my-mighty-app                                        │
│  Workspace: rnv                                                              │
│  Project Title: My Mighty App                                                │
│  Project Version: 0.1.0                                                      │
│  App ID: com.mycompany.my-mighty-app                                         │
│  Project Template: @rnv/template-starter@0.36.1                              │
│  Git Enabled: false                                                          │
│                                                                              │
│  Project Platforms:                                                          │
│  ios, android, androidtv, firetv, androidwear, web, webtv, tizen,            │
│  tvos, webos, macos, windows, tizenwatch, tizenmobile, kaios,                │
│  firefoxos, firefoxtv, chromecast, xbox                                      │
│                                                                              │
│  Project Structure:                                                          │
│                                                                              │
│  my-mighty-app                                                               │
│   ├── appConfigs            # Application flavour configuration files/assets │
│   │   └── [APP_ID]          # Example application flavour                    │
│   │       ├── assets        # Platform assets injected to ./platformAssets   │
│   │       ├── builds        # Platform files injected to ./platformBuilds    │
│   │       ├── fonts             # Folder for all custom fonts                │
│   │       ├── plugins           # Multi-platform plugins injections          │
│   │       └── renative.json # Application flavour config                     │
│   ├── platformAssets        # Generated cross-platform assets                │
│   ├── platformBuilds        # Generated platform app projects                │
│   ├── src                   # Source code files                              │
│   ├── index.*.js            # Entry files                                    │
│   └── renative.json         # ReNative project configuration                 │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

Is all this correct? Yes
```

### Install Mighty Apps Builder

Then, install Mighty Apps Builder as below:
```bash npm2yarn
npm install mightyappsbuilder
```

Add the following package.json scripts:

```json title="package.json" showLineNumbers
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }
}
```

## Run the Development Platform
1. Run the following command to start the dev server:
    ```bash npm2yarn
    $ npm run dev
    ```
2. Visit https://localhost:3000 to open the builder
3. Happy Building! 😊🚀

## Next Steps
1. Learn more about Mighty Apps Builder Development Platform
2. Learn more about the [Project Structure](./project-structure.md)