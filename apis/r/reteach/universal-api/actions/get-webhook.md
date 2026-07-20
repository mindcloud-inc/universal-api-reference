# Reteach: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-webhook?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-webhook?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | The id of the webhook subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "id": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string |  |
| `id` | string |  |
| `target` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /subscription/{subscriptionId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

