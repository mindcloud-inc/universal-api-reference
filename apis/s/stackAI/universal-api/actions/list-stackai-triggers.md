# Stack AI: List StackAI Triggers



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-triggers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/list-stackai-triggers?${params}`, {
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
      "provider_id": "string",
      "triggers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `provider_id` | string | The provider identifier. |
| `triggers` | array<string> | Available trigger identifiers for the provider. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/triggers` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stackai-triggers.md) for the provider-specific parameters and requirements.

