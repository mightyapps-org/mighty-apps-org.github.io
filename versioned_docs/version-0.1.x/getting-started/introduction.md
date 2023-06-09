# Installation
Install Mighty Apps Builder, its dependencies, and complete necessary setup.

## Dependencies
- Node.js 14.17.5 or later (See supported versions [here](https://github.com/mightyapps-org/builder/blob/master/SECURITY.md))
- ReNative version [...] or later (Check installed version with ```rnv --version```) To install ReNative, run:
    ```bash npm2yarn
    $ npm install rnv -g
    ```
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


```bash title=">_ Terminal"
rnv new
```

Follow the RNV set-up steps to create a new project.

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