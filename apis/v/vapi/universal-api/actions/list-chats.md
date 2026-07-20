# Vapi: List Chats

Retrieves a list of chats from Vapi.

```
GET https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-chats?${params}`, {
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
| `id` | string | no | This is the unique identifier for the chat to filter by. |
| `assistantId` | string | no | This is the unique identifier for the assistant that will be used for the chat. |
| `assistantIdAny` | string | no | Filter by multiple assistant IDs. Provide as comma-separated values. |
| `squadId` | string | no | This is the unique identifier for the squad that will be used for the chat. |
| `sessionId` | string | no | This is the unique identifier for the session that will be used for the chat. |
| `previousChatId` | string | no | This is the unique identifier for the previous chat to filter by. |
| `page` | number | no | This is the page number to return. Defaults to 1. |
| `sortOrder` | string | no | This is the sort order for pagination. Defaults to 'DESC'. |
| `limit` | number | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | string | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | string | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | string | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | string | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | string | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | string | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | string | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | string | no | This will return items where the updatedAt is less than or equal to the specified value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "results": [
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
| `metadata` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Vapi API, this operation is `GET /chat` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

