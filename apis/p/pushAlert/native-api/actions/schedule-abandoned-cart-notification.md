# Schedule Abandoned Cart Notification with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/abandonedCart`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Schedule Abandoned Cart Notification](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-abandoned-cart-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber` | body | `string` | yes | Subscriber ID for the abandoned cart event. |
| `extra_info` | body | `string` | no | JSON object string with optional first_name and total_items values. |
