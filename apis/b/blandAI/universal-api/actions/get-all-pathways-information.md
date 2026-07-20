# Bland AI: Get All Pathways Information

Retrieves pathways from your Bland AI account.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-all-pathways-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-all-pathways-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/get-all-pathways-information?${params}`, {
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

Through the native Bland AI API, this operation is `GET /v1/pathway` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-pathways-information.md) for the provider-specific parameters and requirements.

