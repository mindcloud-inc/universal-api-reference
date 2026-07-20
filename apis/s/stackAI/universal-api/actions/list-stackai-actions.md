# Stack AI: List StackAI Actions



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-actions?${params}`, {
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
      "actions": [
        "string"
      ],
      "provider_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<string> | Available action identifiers for the provider. |
| `provider_id` | string | The provider identifier. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/actions` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stackai-actions.md) for the provider-specific parameters and requirements.

