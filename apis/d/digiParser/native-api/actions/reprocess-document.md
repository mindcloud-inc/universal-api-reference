# Reprocess Document with DigiParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/process/:parserId/reprocess`
- **Base URL:** `https://app.digiparser.com`
- **Official documentation:** [Reprocess Document](https://www.digiparser.com/docs/api/reprocessDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parserId` | path | `string` | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentId` | body | `string` | no | Existing document UUID to reprocess. |
| `externalId` | body | `string` | no | External ID of the document to reprocess for this parser. |
