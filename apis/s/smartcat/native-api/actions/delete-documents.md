# Delete Documents with Smartcat

Deletes documents from the current Smartcat account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/integration/v1/document`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Delete Documents](https://developers.smartcat.com/api/#delete-one-or-several-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | query | `string` | yes | One or more document IDs in documentId_targetLanguageId format Send multiple values as a string separated by `,`. |
