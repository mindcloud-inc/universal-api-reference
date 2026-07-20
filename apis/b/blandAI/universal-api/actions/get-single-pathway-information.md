# Bland AI: Get Single Pathway Information

Retrieves a pathway from your Bland AI account.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-single-pathway-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-single-pathway-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-single-pathway-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "edges": [
        {}
      ],
      "name": "Ava Chen",
      "nodes": [
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
| `description` | string |  |
| `edges` | array<object> |  |
| `name` | string |  |
| `nodes` | array<object> |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/pathway/{pathway_id}` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-pathway-information.md) for the provider-specific parameters and requirements.

