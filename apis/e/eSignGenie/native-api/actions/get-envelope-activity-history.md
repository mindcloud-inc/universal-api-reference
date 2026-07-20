# Get Envelope Activity History with eSign Genie

Retrieves envelope activity history from eSign Genie.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/viewActivityHistory`
- **Base URL:** `https://na1.foxitesign.foxit.com/api`
- **Official documentation:** [Get Envelope Activity History](https://docs.developer-api.foxit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `number` | yes | The Foxit eSign envelope ID whose activity history should be returned. |
