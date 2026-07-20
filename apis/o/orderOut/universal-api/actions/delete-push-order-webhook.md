# OrderOut: Delete Push Order Webhook

Deletes a push order webhook from OrderOut.

```
DELETE https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/delete-push-order-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OrderOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/delete-push-order-webhook?connectionId=$CONNECTION_ID&pushOrderWebhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pushOrderWebhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/delete-push-order-webhook?${params}`, {
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
| `pushOrderWebhookId` | string | yes | Push order webhook identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OrderOut API returns.

## Native endpoint

Through the native OrderOut API, this operation is `DELETE /api/webhooks/push_order/:push_order_webhook_id` (base URL `https://api.orderout.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-push-order-webhook.md) for the provider-specific parameters and requirements.

