# List Link Sources with Sakari SMS

Retrieves link sources from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/links/:linkId/sources`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Link Sources](https://developer.sakari.io/api-reference/links/fetch-link-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | — |
| `sources` | query | `string` | no | Sources to analyse |
