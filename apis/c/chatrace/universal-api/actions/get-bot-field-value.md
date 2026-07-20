# Chatrace: Get Bot Field Value

Retrieves a bot field value from Chatrace.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-bot-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-bot-field-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-bot-field-value?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "type": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `type` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /accounts/bot_fields/:bot_field_id` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-field-value.md) for the provider-specific parameters and requirements.

