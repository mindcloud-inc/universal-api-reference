# Mekari Qontak: Mark All Notifications as Read

Marks all notifications as read in Mekari Qontak.

```
PUT https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/mark-all-notifications-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mekari Qontak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/mark-all-notifications-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/mark-all-notifications-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "developerMessage": "string",
        "errorCode": "string",
        "info": "string",
        "message": "string",
        "status": 1,
        "type": "string"
      },
      "response": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `meta.developerMessage` | string |  |
| `meta.errorCode` | string |  |
| `meta.info` | string |  |
| `meta.message` | string |  |
| `meta.status` | number |  |
| `meta.type` | string |  |
| `response` | array<object> |  |

## Native endpoint

Through the native Mekari Qontak API, this operation is `PUT qontak/crm/notifications/mark_all_as_read` (base URL `https://api.mekari.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-all-notifications-as-read.md) for the provider-specific parameters and requirements.

