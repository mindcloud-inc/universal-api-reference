# Download Envelope Files with eSign Genie

Retrieves envelope files from eSign Genie.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/download`
- **Base URL:** `https://na1.foxitesign.foxit.com/api`
- **Official documentation:** [Download Envelope Files](https://docs.developer-api.foxit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `number` | yes | The Foxit eSign envelope ID whose files should be downloaded. |
