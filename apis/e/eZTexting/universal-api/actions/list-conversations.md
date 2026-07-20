# EZ Texting: List Conversations

Retrieves conversations from EZ Texting.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-conversations?${params}`, {
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
| `filters[archived][eq]` | string | no | Filter conversations by archive state |
| `filters[from][eq]` | string | no | Filter conversations by sender number Example: `(737) 337-8315`. |
| `filters[optType][eq]` | string | no | Filter conversations by opt type |
| `filters[query][eq]` | string | no | Filter conversations by text query |
| `filters[unread][eq]` | string | no | Filter conversations by unread state |
| `page` | number | no | Page offset starting at 0 |
| `size` | number | no | Page size |
| `sort` | string | no | Sort field and direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "contactName": "Ava Chen",
      "contactNumber": "string",
      "optIn": true,
      "optOut": true,
      "unreadCount": 1,
      "userNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `contactName` | string |  |
| `contactNumber` | string |  |
| `optIn` | boolean |  |
| `optOut` | boolean |  |
| `unreadCount` | number |  |
| `userNumber` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `GET /conversations` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

