# Create Space Document with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/spaces/{{space}}/documents`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Create Space Document](https://docs.docuwriter.ai/docuwriterai-api-docs/92056)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Document body content. |
| `parent_id` | body | `number` | no | Optional parent folder ID. |
| `path` | body | `string` | no | Slash-delimited folder path. |
| `space` | path | `number` | yes | ID of the Space. |
| `title` | body | `string` | yes | Document title. |
| `type` | body | `string` | no | Storage format: blank or markdown. |
