# hubspot-client-template

## HubSpot Local Development

Please check KB Articles:

- [Local Development Tooling: CLI Reference](https://developers.hubspot.com/docs/cms/developer-reference/local-development-cli)
- [Quick start guide to developing on the HubSpot CMS](https://developers.hubspot.com/docs/cms/guides/getting-started)

## Setup local environment

Clone repository to your local machine

```bash
git clone git+https://github.com/sunnypixels-io/hubspot-client-template.git
```

Change current directory

```bash
cd ./hubspot-client-template
```

Install Packages

```bash
npm install
```

### Configure the local development tools (HubSPot Cli)

Run `hs init` to connect the tools to your HubSpot account. This command will walk you through the following steps:

1. First you’ll be guided to create a personal CMS access key to enable authenticated access to your account via the
   local development tools. You’ll be prompted to press "Enter" when you’re ready to open
   the [Personal CMS Access Key](https://app.hubspot.com/l/personal-access-key) page in your default browser. This page
   will allow you to view or generate your personal access key, if necessary. (Note: You’ll need to select at least
   the "Design Manager" permission in order to complete this tutorial.) Copy your access key and paste it in the
   terminal.
2. Next, you’ll enter a name for the account. This name is only seen and used by you, For example, you might use "
   sandbox" if you're using a developer sandbox or "company.com" if you’re using a full customer account. This name will
   be used when running commands.

Once you've completed this simple `init` flow, you'll see a success message confirming that a configuration
file, `hubspot.config.yml`, has been created in your current directory.

##### File `hubspot.config.yml` contains your personal access keys

##### Please be sure you are not track file `hubspot.config.yml` and its include to `.gitignore`

## NPM Scripts

- `npm run fetch` - Fetch files from HubSpot (Be sure you commit local changes first before run this command, bc its
  override your local files and any changes)
- `npm run push` - upload local files to HubSpot
- `npm run watch` - run Watch process to upload files to HubSpot when you save the file ore create new one.

## Workflow

1. Always First commit your local changes
2. Second step use `npm run fetch` to be sure, your local files up to date
3. Two ways:

    - `npm run push` - Edit files locally and push then to HS when you are ready (please be sure you fetch first)
    - `npm run watch` - edit files, and save them, the HSCli will upload files on fly, and you will see how preview
      pages updates in live-reload mode

# May 4th be with you

<img src="https://cdn.sunnypixels.io/imgs/yoda-close-up.jpg" alt="May 4th be with you" width="280">