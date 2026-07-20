# Get Pull Request Review with Calibre

Retrieves a pull request review by branch from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Get Pull Request Review](https://calibreapp.com/docs/automation/pull-request-reviews#view-an-existing-pull-request-review)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.site` | body | `string` | yes |
| `variables.branch` | body | `string` | yes |
