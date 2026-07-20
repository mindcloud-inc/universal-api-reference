# List Links By Tag with Raven Tools

Retrieves links by tag from Raven Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [List Links By Tag](https://api.raventools.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain to inspect for link records. |
| `tag` | query | `string` | yes | The required tag filter for returned links. |
