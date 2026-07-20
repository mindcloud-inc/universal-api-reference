# Download Single Document PDF with eSign Genie

Retrieves a document PDF from eSign Genie.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/document/download`
- **Base URL:** `https://na1.foxitesign.foxit.com/api`
- **Official documentation:** [Download Single Document PDF](https://docs.developer-api.foxit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docNumber` | query | `number` | yes | The document number within the envelope. |
| `folderId` | query | `number` | yes | The Foxit eSign envelope ID that contains the document. |
