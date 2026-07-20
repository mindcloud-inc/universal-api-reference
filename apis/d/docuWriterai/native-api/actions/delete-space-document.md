# Delete Space Document with DocuWriter.ai

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/spaces/{{space}}/documents/{{spaceMenuItem}}`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Delete Space Document](https://docs.docuwriter.ai/docuwriterai-api-docs/92057)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `number` | yes | ID of the Space. |
| `spaceMenuItem` | path | `number` | yes | ID of the Space document to delete. |
