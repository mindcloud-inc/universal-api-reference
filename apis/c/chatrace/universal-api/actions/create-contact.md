# Chatrace: Create Contact

Creates a new contact in Chatrace.

```
POST https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/create-contact', {
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
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "locale": "string",
      "page_id": 1,
      "profile_pic": "string",
      "subscribed": 1,
      "subscribed_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `locale` | string |  |
| `page_id` | number |  |
| `profile_pic` | string |  |
| `subscribed` | number |  |
| `subscribed_date` | string |  |

## Native endpoint

Through the native Chatrace API, this operation is `POST /contacts` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

