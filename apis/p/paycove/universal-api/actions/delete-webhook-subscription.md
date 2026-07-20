# Paycove: Delete Webhook Subscription

Deletes a webhook subscription from Paycove.

```
DELETE https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-webhook-subscription?connectionId=$CONNECTION_ID&targetUrl=https%3A%2F%2Fexample.com%2Fpaycove-webhooks&event=invoice_paid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetUrl": "https://example.com/paycove-webhooks",
  "event": "invoice_paid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/delete-webhook-subscription?${params}`, {
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
| `targetUrl` | string | yes | Target webhook URL to delete. Example: `https://example.com/paycove-webhooks`. |
| `event` | string | yes | Webhook event type to delete. Example: `invoice_paid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `DELETE hooks` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-subscription.md) for the provider-specific parameters and requirements.

