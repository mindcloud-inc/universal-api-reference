# Delete card tokens with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/deleteToken`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Delete card tokens](https://docs.nexiopay.com/reference/deletecardtokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tokens[]` | body | `array<string>` | yes | Array of saved card tokens to delete. |
