# Delete Abandoned Cart Notification with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/abandonedCart/delete`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Delete Abandoned Cart Notification](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-abandoned-cart-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber` | body | `string` | yes | Subscriber ID for the completed order event. |
