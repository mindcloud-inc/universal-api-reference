# Upload via URL with DigiParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/process/:parserId/urls`
- **Base URL:** `https://app.digiparser.com`
- **Official documentation:** [Upload via URL](https://www.digiparser.com/docs/api/uploadDocumentUrls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parserId` | path | `string` | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `urls[]` | body | `array<string>` | yes | URLs pointing to document files, up to 20 per request. |
| `folderId` | body | `string` | no | Optional folder UUID to assign created documents to that folder. |
| `externalIds[]` | body | `array<string>` | no | Optional array of external IDs, one per URL. |
| `custom[]` | body | `array<object>` | no | Optional array of tracking objects, one per URL. |
