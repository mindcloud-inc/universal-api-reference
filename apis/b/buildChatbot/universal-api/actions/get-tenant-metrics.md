# BuildChatbot: Get Tenant Metrics

Retrieves tenant usage metrics from BuildChatbot.

```
GET https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-tenant-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-tenant-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-tenant-metrics?${params}`, {
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
      "characters": {},
      "chatbots": {},
      "messages": {},
      "qaLimit": {},
      "storage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `characters` | object | Tenant character quota and usage. |
| `chatbots` | object | Tenant chatbot quota and usage. |
| `messages` | object | Tenant message quota and usage. |
| `qaLimit` | object | Tenant question-answer limits. |
| `storage` | object | Tenant storage quota and usage. |

## Native endpoint

Through the native BuildChatbot API, this operation is `GET /user/get_all_tenant_metrics` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-metrics.md) for the provider-specific parameters and requirements.

