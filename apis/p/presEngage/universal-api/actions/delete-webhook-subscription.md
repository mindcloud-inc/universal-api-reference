# PresEngage: Delete Webhook Subscription

Deletes an existing webhook subscription from PresEngage.

```
DELETE https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/delete-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PresEngage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/delete-webhook-subscription?connectionId=$CONNECTION_ID&subscriptionId=sub_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "sub_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/delete-webhook-subscription?${params}`, {
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
| `subscriptionId` | string | yes | Webhook subscription ID to unsubscribe. Example: `sub_12345`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PresEngage API returns.

## Native endpoint

Through the native PresEngage API, this operation is `DELETE /hooks/unsubscribe/:subscriptionId` (base URL `https://shared.presengage.com/functions/v1/presengage-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-subscription.md) for the provider-specific parameters and requirements.

