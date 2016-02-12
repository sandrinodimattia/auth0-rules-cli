# Auth0 Rules CLI

A small CLI tool to manage your rules in Auth0.

## Configuration

Set the following environment variables or update your **config.json** file:
 
 - `AUTH0_DOMAIN`: Your Auth0 domain (eg: myaccount.auth0.com or myaccount.myappliance.com)
 - `AUTH0_API_TOKEN`: An API token with permissions to read/create/update/delete rules
 
You might need to make your files executable first:

```bash
chmod +x rules
chmod +x rules-delete
chmod +x rules-deploy
chmod +x rules-list
```
 
## Usage

Make sure you use Node.js 5+ (`nvm use 5`/`nave use 5`).

Listing all of your rules:

```bash
./rules list
```

Create or update a rule:

```bash
./rules deploy --name "Test-User-Registration" --file ./rule-scripts/log-example.js --stage user_registration
```

Delete a rule:

```bash
./rules delete --name "Test-User-Registration" --stage user_registration
```