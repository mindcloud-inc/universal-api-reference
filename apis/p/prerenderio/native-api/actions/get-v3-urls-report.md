# List Urls Report with Prerender.io

Retrieves a URLs report from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/urls/report`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Urls Report](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | query | `string` | yes |
| `next` | query | `string` | no |
| `take` | query | `number` | no |
