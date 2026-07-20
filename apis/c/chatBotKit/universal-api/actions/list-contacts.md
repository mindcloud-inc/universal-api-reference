# ChatBotKit: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | The cursor to use for pagination |
| `order` | list | no | The order of the paginated items One of: `asc`, `desc`. |
| `take` | number | no | The number of items to retrieve |
| `meta` | object | no | Key-value pairs to filter the partner users by metadata |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "createdAt": 1,
          "description": "string",
          "email": "ava@example.com",
          "fingerprint": "string",
          "id": "string",
          "name": "Ava Chen",
          "nick": "string",
          "phone": "string",
          "preferences": "string",
          "updatedAt": 1,
          "verifiedAt": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `items[].createdAt` | number |  |
| `items[].description` | string |  |
| `items[].email` | string |  |
| `items[].fingerprint` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].nick` | string |  |
| `items[].phone` | string |  |
| `items[].preferences` | string |  |
| `items[].updatedAt` | number |  |
| `items[].verifiedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /contact/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

