# Port API AI: Get AI Invocation Quota

Retrieves AI invocation quota usage from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation-quota
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation-quota?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation-quota?${params}`, {
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
      "monthlyQuotaUsage": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monthlyQuotaUsage` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /quota/ai-invocations` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-invocation-quota.md) for the provider-specific parameters and requirements.

