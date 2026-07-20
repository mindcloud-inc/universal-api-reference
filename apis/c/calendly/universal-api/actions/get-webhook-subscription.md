# Calendly: Get Webhook Subscription

Retrieves a webhook subscription from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID&webhook_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhook_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-webhook-subscription?${params}`, {
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
| `webhook_uuid` | string | yes | Webhook subscription UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `GET /webhook_subscriptions/:webhook_uuid` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

