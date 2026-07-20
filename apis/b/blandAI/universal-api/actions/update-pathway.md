# Bland AI: Update Pathway

Updates an existing pathway in Bland AI.

```
PUT https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-pathway
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-pathway" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-pathway', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "edges": [
        {}
      ],
      "nodes": [
        {}
      ],
      "pathway_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `edges` | array<object> |  |
| `nodes` | array<object> |  |
| `pathway_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v1/pathway/{pathway_id}` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pathway.md) for the provider-specific parameters and requirements.

