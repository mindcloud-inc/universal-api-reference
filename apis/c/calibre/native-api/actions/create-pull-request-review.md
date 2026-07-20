# Create Pull Request Review with Calibre

Creates a new pull request review in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Create Pull Request Review](https://calibreapp.com/docs/automation/pull-request-reviews#create-a-pull-request-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.title` | body | `string` | yes | Title shown for the pull request review. |
| `variables.sha` | body | `string` | yes | Current HEAD commit SHA of the branch being tested. |
| `variables.branch` | body | `string` | yes | Branch name being reviewed. |
| `variables.url` | body | `string` | yes | Preview deployment URL for the pull request review. |
