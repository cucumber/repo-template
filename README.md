# Cucumber repo template

Contains templates that should be used in all other Cucumber repositories

## GitHub templates

Stores the templates used for issues and pull requests creations on GitHub. Synchronize your repo using this command:

```bash
./scripts/sync_github_templates <path to your repository>

# Example: ./scripts/sync_github_templates ~/dev/cucumber/cucumber-ruby
```

This script will delete the existing templates in the `.github` folder in your repository and add the new ones.

## GitHub labels

All repositories should have a common set of labels to tag the issues and PRs. A script is provided in `scripts/sync_github_labels`. You will need Ruby installed and the `octokit` gem available:

```bash
export GITHUB_TOKEN="your token"

# To create the template labels
scripts/sync_github_labels <repository-name> --create-templates

# To delete GitHub's default labels
scripts/sync_github_labels <repository-name> --delete-defaults

# To run both command at once
scripts/sync_github_labels <repository-name> --init-repo
```
