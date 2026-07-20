# Generate Draft From Knowledge with Colossyan

Creates a draft from structured knowledge in Colossyan.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.colossyan.com/api/knowledge-to-draft/generate-draft`
- **Base URL:** `https://app.colossyan.com/api/v1`
- **Official documentation:** [Generate Draft From Knowledge](https://docs.colossyan.com/experimental/knowledge-to-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `summary` | body | `object` | yes | Structured summary object with title, description, and chapters. |
| `templateId` | body | `string` | no | Optional template ID for the generated draft. |
