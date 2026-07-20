# Follow Recalculate URL with Wolfram Alpha

Retrieves recalculated results from a Wolfram Alpha query URL.

## Endpoint

- **Method:** `GET`
- **Path:** `{{recalculateUrl}}`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Follow Recalculate URL](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recalculateUrl` | query | `string` | yes | Full recalculate URL returned by a prior Full Results response. |
