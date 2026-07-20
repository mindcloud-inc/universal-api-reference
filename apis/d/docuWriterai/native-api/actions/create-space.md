# Create Space with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/spaces`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Create Space](https://docs.docuwriter.ai/docuwriterai-api-docs/358013)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Space description. |
| `is_public` | body | `boolean` | no | Whether the new Space is public. |
| `name` | body | `string` | yes | Space name. |
| `slug` | body | `string` | no | Optional URL slug for public Spaces. |
