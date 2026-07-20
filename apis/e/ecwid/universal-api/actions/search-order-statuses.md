# Ecwid: Search Order Statuses

Finds order statuses in Ecwid.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-order-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultStatus": true,
      "enabled": true,
      "orderStatusType": "string",
      "sendNotificationWhenStatusIsAssigned": true,
      "statusId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultStatus` | boolean | Whether the status is an Ecwid default status. |
| `enabled` | boolean | Whether the status can currently be assigned. |
| `orderStatusType` | string | Whether the status applies to payment or fulfillment. |
| `sendNotificationWhenStatusIsAssigned` | boolean | Whether Ecwid notifies customers when the status is assigned. |
| `statusId` | string | Ecwid order status identifier. |

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/profile/order_statuses` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-order-statuses.md) for the provider-specific parameters and requirements.

