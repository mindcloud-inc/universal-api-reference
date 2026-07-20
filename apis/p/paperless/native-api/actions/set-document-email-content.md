# Set Document Email Content with Paperless

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:id`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Set Document Email Content](https://developers.paperless.io/docs/api/ec1d64419e849-setting-the-e-mail-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Paperless document ID. |
| `settings` | body | `object` | yes | The full settings object including mail subject, content, and signature. |
