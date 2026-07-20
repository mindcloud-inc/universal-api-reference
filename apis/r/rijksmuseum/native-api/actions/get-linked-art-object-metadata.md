# Get Linked Art Object Metadata with Rijksmuseum

## Endpoint

- **Method:** `GET`
- **Path:** `/{{metadataObjectId}}`
- **Base URL:** `https://data.rijksmuseum.nl`
- **Official documentation:** [Get Linked Art Object Metadata](https://data.rijksmuseum.nl/docs/http/content-negotiation-arguments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadataObjectId` | path | `string` | yes | Numeric Rijksmuseum metadata object ID, such as 200107928 for The Night Watch. |
