# Create Site with GitBook

Creates a new site in GitBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:organizationId/sites`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Create Site](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | — |
| `spaces[]` | body | `array<string>` | no | Send multiple values as a array. |
| `title` | body | `string` | no | Title of the site. Maximum length: 128. |
| `type` | body | `string` | no | — |
| `visibility` | body | `string` | no | — |
