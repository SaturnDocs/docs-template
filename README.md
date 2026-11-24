# Documentation site template

Use this template to start a SaturnDocs site with an introduction, a quickstart, and a glossary.
Replace the product name in `docs/docs.json` and the placeholder text in `docs/pages/`.

## Create the repository on GitHub

Choose **Use this template**, then **Create a new repository**. Name your repository and create it.

## Create the repository with a coding agent

Ask your coding agent to run this command. Replace `<name>` with your new repository name.

```sh
gh repo create <name> --private --template SaturnDocs/docs-template --clone
```

## Connect the repository

1. Open the SaturnDocs dashboard.
2. Install the SaturnDocs GitHub App on your new repository.
3. Select your repository, set the branch to `main`, and set the docs folder to `docs`.
4. Connect the repository. SaturnDocs starts the first build at once.

## Check changes locally

Run the check from the repository root before each push.

```sh
npx saturndocs@latest check docs
```

Fix every error. Push to the connected branch to publish your changes.
