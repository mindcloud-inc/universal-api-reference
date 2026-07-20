# Chatrace: Get Contact

Retrieves a contact record from Chatrace.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-contact?${params}`, {
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

Through the native Chatrace API, this operation is `GET /contacts/:contact_id` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

