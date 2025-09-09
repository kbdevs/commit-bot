# commit-bot

A GitHub Action that automatically increments a counter in `numeral.txt` and commits changes with random probability to generate 1-7 commits per day.

## How it works

- **Schedule**: Runs every 2 hours (12 times per day)
- **Random Commits**: 35% chance to actually commit changes
- **Expected Activity**: 3-5 commits per day on average, with natural variance of 1-7 commits
- **Counter**: Tracks incrementing numbers in `numeral.txt`

## Features

- ✅ Automated scheduling via GitHub Actions cron
- ✅ Random commit probability for natural variability
- ✅ Clean commit messages showing increment progression
- ✅ Uses built-in `GITHUB_TOKEN` for authentication
- ✅ Manual trigger support via `workflow_dispatch`

## Environment Variables

The action uses the following:
- `GITHUB_TOKEN` (automatically provided by GitHub Actions)
- Environment variables are read but not currently used (ready for future extensions)

## Files

- `numeral.txt` - Contains the current counter value
- `.github/workflows/increment-commit.yml` - The main workflow definition

## Manual Testing

You can manually trigger the workflow from the Actions tab in GitHub to test it immediately.