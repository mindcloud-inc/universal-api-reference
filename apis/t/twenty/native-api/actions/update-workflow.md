# Update Workflow with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/workflows/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Workflow](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `lastPublishedVersionId` | body | `string` | no |
| `statuses[]` | body | `array<string>` | no |
| `name` | body | `string` | no |
