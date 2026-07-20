# Import Glossary with Smartcat

Creates a glossary import task in Smartcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/glossary/import`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Import Glossary](https://developers.smartcat.com/api/#create-a-task-for-importing-concepts-from-a-glossary-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `glossaryId` | query | `string` | yes | Glossary ID. |
| `clearBeforeImport` | query | `boolean` | yes | Delete existing glossary concepts before import. |
| `file` | body | `file` | yes | Glossary import file. |
