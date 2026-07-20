# Order Desk: Get Store Settings

Retrieves store settings from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-store-settings?${params}`, {
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
      "folders": {},
      "id": 1,
      "name": "Ava Chen",
      "settings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folders` | object | Folder map keyed by folder ID. |
| `id` | number | Order Desk internal store ID. |
| `name` | string | Store name. |
| `settings` | object | Store configuration settings. |

## Native endpoint

Through the native Order Desk API, this operation is `GET /store` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store-settings.md) for the provider-specific parameters and requirements.

