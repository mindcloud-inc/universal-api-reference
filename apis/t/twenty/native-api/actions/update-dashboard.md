# Update Dashboard with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/dashboards/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Dashboard](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `title` | body | `string` | no |
| `pageLayoutId` | body | `string` | no |
