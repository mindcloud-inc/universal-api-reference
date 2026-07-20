# Search Videos with Freepik

Finds Freepik videos by search term and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Search Videos](https://docs.freepik.com/api-reference/videos/videos-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Video search term. Freepik returns a validation error when omitted. |
| `page` | query | `number` | no | One-based videos page to request. |
