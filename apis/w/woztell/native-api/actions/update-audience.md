# Update Audience with Woztell

Updates an audience in your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Update Audience](https://doc.woztell.com/open-api-reference/#mutation-updateAudience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.audienceId` | body | `string` | yes | Raw Woztell audience _id to update. |
| `variables.input.etag` | body | `string` | yes | Current Woztell audience etag for optimistic concurrency. |
| `variables.input.description` | body | `string` | no | Updated audience description. |
