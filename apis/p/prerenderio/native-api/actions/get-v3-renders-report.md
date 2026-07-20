# List Renders Report with Prerender.io

Retrieves a renders report from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/renders/report`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Renders Report](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | query | `string` | yes |
| `from` | query | `string` | yes |
| `next` | query | `string` | no |
| `take` | query | `number` | no |
| `to` | query | `string` | yes |
