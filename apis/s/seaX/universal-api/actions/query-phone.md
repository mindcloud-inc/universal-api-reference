# SeaX: Query Phone



```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/query-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/query-phone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/query-phone', {
  method: 'POST',
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
      "country": "string",
      "dnc_reply_message": "string",
      "enabled": true,
      "enabled_dnc_reply": true,
      "enabled_generic_reply": true,
      "generic_reply_message": "string",
      "name": "Ava Chen",
      "phone": "string",
      "source": {},
      "type": {},
      "whatsapp_device_id": "string",
      "whatsapp_status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `dnc_reply_message` | string |  |
| `enabled` | boolean |  |
| `enabled_dnc_reply` | boolean |  |
| `enabled_generic_reply` | boolean |  |
| `generic_reply_message` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `source` | object |  |
| `type` | object |  |
| `whatsapp_device_id` | string |  |
| `whatsapp_status` | object |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /phones/query_phone` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-phone.md) for the provider-specific parameters and requirements.

