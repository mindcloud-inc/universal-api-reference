# Langbase: Create Memory



```
POST https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Memory name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chunkOverlap": 1,
      "chunkSize": 1,
      "embeddingModel": "string",
      "name": "Ava Chen",
      "ownerLogin": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkOverlap` | number |  |
| `chunkSize` | number |  |
| `embeddingModel` | string |  |
| `name` | string |  |
| `ownerLogin` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Langbase API, this operation is `POST v1/memory` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-memory.md) for the provider-specific parameters and requirements.

