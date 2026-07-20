# Create Webhook with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Webhook](https://developers.kommo.com/reference/add-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | Webhook destination URL. |
| `settings[]` | body | `array<string>` | yes | Webhook trigger events. Passed as an array of events. |
| `sort` | body | `number` | no | Webhook sort order. |
