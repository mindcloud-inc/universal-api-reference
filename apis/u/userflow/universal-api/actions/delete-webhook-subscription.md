# Userflow: Delete Webhook Subscription

Deletes an existing webhook subscription from Userflow.

```
DELETE https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-webhook-subscription?connectionId=$CONNECTION_ID&webhookSubscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookSubscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-webhook-subscription?${params}`, {
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
| `webhookSubscriptionId` | string | yes | ID of the webhook subscription to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the webhook subscription was deleted. |
| `id` | string | Deleted webhook subscription ID. |
| `object` | string | Returned object type. |

## Native endpoint

Through the native Userflow API, this operation is `DELETE /webhook_subscriptions/:webhook_subscription_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-subscription.md) for the provider-specific parameters and requirements.

