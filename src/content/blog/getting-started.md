---
title: Getting Started
description: How to quickly build your personal website (blog/portfolio) with Astro AntfuStyle Theme
pubDate: 2024-10-04
lastModDate: ''
toc: true
share: true
ogImage: true
---

This post outlines the essential steps to quickly set up your personal website using the [Astro AntfuStyle Theme](https://github.com/lin-stephanie/astro-antfustyle-theme). Each step may involve more detailed content, requiring you to consult other posts for further information.

## Preparation (Skip If You're a Developer)

To build your website with this theme, it's recommended to:

- [Install Node.js](https://nodejs.org/en/download/package-manager) for running and developing the project locally.
- [Install pnpm](https://pnpm.io/installation) for managing dependencies.
- [Configure Git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git) for version control.
- [Register on GitHub](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github) for cloud hosting.
- [Install VS Code](https://code.visualstudio.com/download) for code editing. [Set up Git and sign in to GitHub](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git#_set-up-git-in-vs-code).
- Familiarity with [Astro](https://docs.astro.build/en/getting-started/) and [basic front-end knowledge](https://medium.com/swlh/web-development-fundamentals-for-newcomers-part-1-front-end-2e77f830754e) is a plus.

These are ideal conditions, but feel free to substitute with tools you're comfortable with.

## Create Your Project

Create your project from the latest theme version in two ways:

**Use GitHub**

Create a new repository in your GitHub account by clicking ["Use this template"](https://github.com/new?template_name=astro-antfustyle-theme&template_owner=lin-stephanie) (without commit history) or ["Fork"](https://github.com/lin-stephanie/astro-antfustyle-theme/fork) (preserves commit history) , then clone it locally:

```bash
# If SSH is not configured
git clone https://github.com/[YOUR_USERNAME]/[YOUR_REPO_NAME].git

# If SSH is configured
git clone git@github.com:[YOUR_USERNAME]/[YOUR_REPO_NAME].git
```

**Use CLI**

Run the following commands in your desired directory to start locally:

```bash
# npm 6.x
npm create astro@latest --template lin-stephanie/astro-antfustyle-theme

# npm 7+, extra double-dash is needed
npm create astro@latest -- --template lin-stephanie/astro-antfustyle-theme

# yarn
yarn create astro --template lin-stephanie/astro-antfustyle-theme

# pnpm
pnpm dlx create-astro --template lin-stephanie/astro-antfustyle-theme
```

> [!tip] If you prefer not to use Git, you can [download the ZIP file](https://github.com/lin-stephanie/astro-antfustyle-theme/archive/refs/heads/main.zip), extract it, and work directly in your local directory.

## Launch the Project

Start the project by running the following commands from the project root (replace `pnpm` with your preferred package manager if needed):

```bash
# Install dependencies
pnpm install

# Start the local dev server (opens at 'http://localhost:4321')
pnpm dev
```

You can explore the current theme freely. Additionally, the following commands are available:

| Command                                     | Description                                                                                                                 |
| :------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------- |
| `pnpm install`                              | Installs dependencies                                                                                                       |
| `pnpm dev`                                  | Starts a local development server at `localhost:4321` and opens the site in your browser                                    |
| `pnpm sync`                                 | Generates TypeScript types for Astro modules. [Learn more](https://docs.astro.build/en/reference/cli-reference/#astro-sync) |
| `pnpm check`                                | Runs diagnostics against your project and reports errors to the console                                                     |
| `pnpm build`                                | Build your production site to `./dist/`                                                                                     |
| `pnpm preview`                              | Preview your build locally, before deploying                                                                                |
| `pnpm format`                               | Check code format with Prettier                                                                                             |
| `pnpm format:write`                         | Format code with Prettier                                                                                                   |
| `pnpm lint`                                 | Check code lint with ESLint                                                                                                 |
| `pnpm lint:fix`                             | Lint code with ESLint                                                                                                       |
| `pnpm astro --help`                         | Get help using the [Astro CLI](https://docs.astro.build/en/reference/cli-reference/)                                        |
| `pnpm toolbar:on`<br>`pnpm toolbar:off`<br> | Enable or disable the [Astro Dev Toolbar](https://docs.astro.build/en/guides/dev-toolbar/)                                  |

Here's the translated document based on your requirements and guidelines:

==【加链接】==

> [!note]- This project uses `pnpm` as the package manager, so you’ll need to install it if you haven’t yet.
>
> You can execute `npm install -g pnpm` to [install `pnpm`](https://pnpm.io/installation) globally. Alternatively, you can [enable `corepack`](https://github.com/nodejs/corepack) (allows you to manage package manager versions directly via Node.js) or [install the `ni` tool](https://github.com/antfu-collective/ni) (simplifies running commands across different package managers).
>
> If you want to use a different package manager, make sure to ==convert the project to your chosen package manager== before running its commands.

## Configure the Project

> [!important]- Before configuring, it is advisable to review =="Project Structure"== for an overview of the project and how it’s organized.

Configuration can be done in two steps:

==【加链接】==

- **"Basic Configuration"**: Customize the `src/config.ts` file.
- **"Advanced Configuration"**: Customize the LOGOs, site icons, styles, fonts and footer.

## Authoring Content

Once configured, ensure the project is running correctly in your browser, then start creating or migrating your content. Jump to the section you're interested in:

==【加链接】==

- **"Add New Posts"**: For creating posts, writing tips, and guidelines.
- **"Recreate Current Pages"**: For recreating content for the `/`, `/projects`, `/changelog`, `/streams`, `/feeds`, and `404` pages, as well as creating / deleting pages.
- **"Markdown Syntax Guide"**: Showcase the rendering of Markdown syntax in this theme.
- **"Markdown & MDX Extended Features"**: Extended syntax supported by the theme, including callouts (admonitions/alerts), fully-featured code blocks, image captions and links, video embeddings, styled GitHub links, and more.

## Deploy Your Project

Refer to [Astro’s Deployment Guide](https://docs.astro.build/en/guides/deploy/) to choose your preferred platform and follow its guide. Ensure the `SITE.website` option in the `src/config.ts` is correctly set before deploying!

> [!note]- If you aren’t using GitHub and any other Git provider for deployment, follow the [CLI Deployment Guide](https://docs.astro.build/en/guides/deploy/#cli-deployment) to deploy without a Git repository, such as using [Vercel CLI](https://vercel.com/docs/deployments/deploy-with-vercel-cli#deploying-to-vercel-with-vercel-cli) or [Netlify CLI](https://docs.netlify.com/functions/deploy/#manual-deploys-with-cli).

## Sync Updates

Like other open-source projects, this theme evolves with bug fixes and feature updates. It's crucial to sync these updates with your own customized project. Consult ==**"Sync Update"**== for more details.

Check the ==Changelog== or [Releases](https://github.com/lin-stephanie/astro-antfustyle-theme/releases) to stay informed about theme updates, or consider subscribing to the theme's ==RSS== feed.

## Next Steps

You can dive deeper into the theme through the following sections:

==【加链接】==

- **"Managing Image Assets"**: Best practices for using images in Markdown/MDX.
- **"About Open Graph Images"**: How to customize or auto-generate Open Graph images.
- **"FAQs and Known Issues"**: Get more insights into the theme's details.
- **"Explore Resources and Tools"**: A collection of external resources and helpful tools.

Additionally, feel free to explore the theme's ==tech stack==. For parts not mentioned or clarified in the guide, you might find answers in the [Astro Docs](https://docs.astro.build/en/getting-started/). You can also follow the [Astro Blog](https://astro.build/blog/) or join the [Astro Lounge](https://discord.com/invite/grF4GTXXYm) community.

## Wrapping Up

Congratulations on completing the setup! Hopefully, this theme meets your blogging or portfolio needs.

If you encounter any issues, find errors, or see opportunities for improvement, feel free to join the [discussion](https://github.com/lin-stephanie/astro-antfustyle-theme) or submit an [issue](https://github.com/lin-stephanie/astro-antfustyle-theme/issues) or [pull request](https://github.com/lin-stephanie/astro-antfustyle-theme/pulls). Your feedback is invaluable to making this theme even better!

Thank you for taking the time to read this guide. ❤️