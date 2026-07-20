# Get Space Document with DocuWriter.ai

## Endpoint

- **Method:** `GET`
- **Path:** `/api/spaces/{{space}}/documents/{{spaceMenuItem}}`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Get Space Document](https://docs.docuwriter.ai/docuwriterai-api-docs/92054)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `number` | yes | ID of the Space to query. |
| `spaceMenuItem` | path | `number` | yes | ID of the document within the Space. |
