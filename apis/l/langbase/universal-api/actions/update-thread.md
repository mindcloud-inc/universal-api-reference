# Langbase: Update Thread



```
PUT https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | string | yes | Thread ID to update. |
| `metadata` | object | no | Metadata object to merge into the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "metadata": {},
      "object": "string"
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
| `metadata` | object |  |
| `object` | string |  |

## Native endpoint

Through the native Langbase API, this operation is `POST v1/threads/:threadId` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-thread.md) for the provider-specific parameters and requirements.

