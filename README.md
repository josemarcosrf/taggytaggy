# taggytaggy

This repo contains an example github workflow to create tags automatically
upong `push` or `merge` onto `main`.

## Setting things up

1. Create a Personal Access Token (PAT):

Go to your GitHub account settings.
Navigate to `"Developer settings" > "Personal access tokens."`
Click on "Generate token" and give it the necessary permissions.
At least, it should have repo and workflow scopes.

2. Store the Personal Access Token as a Secret:

In your GitHub repository, go to `"Settings" > "Secrets."`
Click on "New repository secret" and name it `GH_TOKEN`.
Paste the Personal Access Token you generated into the "Value" field.


## Troubleshooting

1. Ensure Correct Permissions for the PAT:

Confirm that the PAT you generated has the necessary permissions. It should have at least the repo and workflow scopes. If you're unsure, you can grant it the write:packages scope as well.
Delete the existing secret (GH_TOKEN) from your repository settings, generate a new PAT, and add it as a new secret.

2. Check Repository Permissions:

Ensure that the GitHub Actions bot (github-actions[bot]) has the necessary permissions to push tags to the repository. Go to your repository settings, navigate to "Manage access," and make sure the GitHub Actions bot has the required permissions.
