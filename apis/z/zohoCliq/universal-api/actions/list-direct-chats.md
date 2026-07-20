# Zoho Cliq: List Direct Chats

Retrieves direct chats from Zoho Cliq.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-direct-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-direct-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-direct-chats?${params}`, {
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
| `limit` | number | no | The number of chats to retrieve. Maximum 100. |
| `modifiedBefore` | string | no | Only include chats whose last message was sent before this time. |
| `modifiedAfter` | string | no | Only include chats whose last message was sent after this time. |
| `drafts` | boolean | no | When true, only chats containing drafts are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chats": [
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
| `chats` | array<object> |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /chats` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-direct-chats.md) for the provider-specific parameters and requirements.

