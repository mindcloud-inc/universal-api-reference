# WhatsScale: List Sessions

Retrieves WhatsApp sessions linked to your WhatsScale account.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-sessions?${params}`, {
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
      "me": {
        "id": "string",
        "pushName": "Ava Chen"
      },
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `me` | object |  |
| `me.id` | string |  |
| `me.pushName` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `GET /api/sessions` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

