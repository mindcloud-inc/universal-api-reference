# Pipefile: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipefile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | Pipefile webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "target": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string | Pipefile event that triggers the webhook. |
| `target` | string | Destination URL for webhook deliveries. |
| `user` | object | Pipefile user associated with the webhook, when returned. |

## Native endpoint

Through the native Pipefile API, this operation is `GET /webhooks/:id/` (base URL `https://api.pipefile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

