# List Links with Raven Tools

Retrieves links for a domain in Raven Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [List Links](https://api.raventools.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain to inspect for link records. |
| `tag` | query | `string` | no | Optional tag used to filter returned links. |
| `limit` | query | `string` | no | Optional number of links to return. Raven defaults to 100 and allows up to 1000. |
| `offset` | query | `string` | no | Optional offset for paginated link retrieval. |
