# Delete Webhooks with Parsio

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Delete Webhooks](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Webhook IDs to delete. |
