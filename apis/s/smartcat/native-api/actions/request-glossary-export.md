# Request Glossary Export with Smartcat

Creates a glossary export task in Smartcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/glossary/export`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Request Glossary Export](https://developers.smartcat.com/api/#create-a-task-for-export-the-glossary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `glossaryId` | query | `string` | yes | Smartcat glossary ID to export. |
