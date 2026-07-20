# Libraria: Create Query (Legacy)

Given a query and an optional conversation ID, get a response from your library.

```
POST https://connect.mindcloud.co/v1/universal/libraria/latest/actions/create-query-legacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Libraria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/create-query-legacy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "libraryId": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/libraria/latest/actions/create-query-legacy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "libraryId": "string",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `libraryId` | string | yes | The ID of the library you are going to ask a question. |
| `query` | string | yes | The question you will make to the library. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | no | Optional. Use this for a continuation of the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "metadata": {},
      "reply": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string |  |
| `metadata` | object |  |
| `reply` | string |  |

## Native endpoint

Through the native Libraria API, this operation is `POST /library/:library_id/query` (base URL `https://api.libraria.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-query-legacy.md) for the provider-specific parameters and requirements.

