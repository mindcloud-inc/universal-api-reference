# ManyChat: Search Subscribers by System Field

Finds subscribers in ManyChat by system field.

```
GET https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-system-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-system-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-system-field?${params}`, {
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
| `email` | string | no |  |
| `phone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "igId": {},
      "igLastInteraction": {},
      "igLastSeen": {},
      "igUsername": {},
      "isFollowupEnabled": true,
      "language": {},
      "lastInputText": {},
      "lastInteraction": {},
      "lastName": "Chen",
      "lastSeen": {},
      "liveChatUrl": "https://example.com",
      "locale": {},
      "name": "Ava Chen",
      "optinEmail": true,
      "optinPhone": true,
      "optinWhatsapp": true,
      "pageId": "string",
      "phone": "string",
      "profilePic": {},
      "status": "string",
      "subscribed": "string",
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "timezone": "string",
      "whatsappPhone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `igId` | object |  |
| `igLastInteraction` | object |  |
| `igLastSeen` | object |  |
| `igUsername` | object |  |
| `isFollowupEnabled` | boolean |  |
| `language` | object |  |
| `lastInputText` | object |  |
| `lastInteraction` | object |  |
| `lastName` | string |  |
| `lastSeen` | object |  |
| `liveChatUrl` | string |  |
| `locale` | object |  |
| `name` | string |  |
| `optinEmail` | boolean |  |
| `optinPhone` | boolean |  |
| `optinWhatsapp` | boolean |  |
| `pageId` | string |  |
| `phone` | string |  |
| `profilePic` | object |  |
| `status` | string |  |
| `subscribed` | string |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `timezone` | string |  |
| `whatsappPhone` | object |  |

## Native endpoint

Through the native ManyChat API, this operation is `GET /fb/subscriber/findBySystemField` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-subscribers-by-system-field.md) for the provider-specific parameters and requirements.

