# Update revision metadata (comment, title, feature metadata) with GrowthBook

Updates metadata for a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/metadata`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update revision metadata (comment, title, feature metadata)](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `version` | path | `number` | yes | — |
| `comment` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `project` | body | `string` | no | — |
| `tags` | body | `list<string>` | no | — |
| `neverStale` | body | `boolean` | no | — |
| `customFields` | body | `object` | no | — |
| `jsonSchema` | body | `object` | no | — |
