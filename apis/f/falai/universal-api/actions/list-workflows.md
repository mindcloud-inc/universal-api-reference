# fal.ai: List Workflows

Retrieves authenticated user workflows from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-workflows?${params}`, {
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
      "has_more": true,
      "next_cursor": "string",
      "total": 1,
      "workflows": [
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
| `has_more` | boolean |  |
| `next_cursor` | string |  |
| `total` | number |  |
| `workflows` | array<object> |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /workflows` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

