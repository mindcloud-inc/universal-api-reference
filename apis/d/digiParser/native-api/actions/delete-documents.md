# Delete Documents with DigiParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/process/:parserId/documents/delete`
- **Base URL:** `https://app.digiparser.com`
- **Official documentation:** [Delete Documents](https://www.digiparser.com/docs/api/deleteDocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parserId` | path | `string` | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentIds[]` | body | `array<string>` | no | Optional list of document UUIDs to delete. |
| `externalIds[]` | body | `array<string>` | no | Optional list of external IDs to delete documents by external ID. |
