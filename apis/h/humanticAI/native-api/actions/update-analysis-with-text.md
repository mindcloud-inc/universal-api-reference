# Update Analysis With Text with Humantic AI

## Endpoint

- **Method:** `POST`
- **Path:** `/user-profile/create`
- **Base URL:** `https://api.humantic.ai/v1`
- **Official documentation:** [Update Analysis With Text](https://api.humantic.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The same identifier used when the original analysis was created. |
| `text` | body | `string` | yes | Additional text to improve confidence for an existing Humantic AI analysis. |
