# Dify: List Conversations

Retrieves conversations from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversations?${params}`, {
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
| `user` | string | no | User identifier. |
| `lastId` | string | no | Cursor for the next page of conversations. |
| `sortBy` | string | no | Sort order for conversations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "inputs": {},
      "introduction": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | string |  |
| `inputs` | object |  |
| `introduction` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Dify API, this operation is `GET /conversations` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

