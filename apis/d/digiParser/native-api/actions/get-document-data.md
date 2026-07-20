# Get Document Data with DigiParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/process/:parserId/files/data`
- **Base URL:** `https://app.digiparser.com`
- **Official documentation:** [Get Document Data](https://www.digiparser.com/docs/api/getDocumentData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parserId` | path | `string` | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentId` | query | `string` | no | Document UUID returned by a DigiParser upload response. |
| `externalId` | query | `string` | no | External tracking ID provided during upload. Use this instead of Document ID when you do not have the DigiParser document UUID. |
