# Climbo 2.0: Delete Subscription

Deletes a webhook subscription from Climbo 2.0.

```
DELETE https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-subscription?${params}`, {
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
| `webhookId` | string | yes | Webhook subscription ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Climbo 2.0 API returns.

## Native endpoint

Through the native Climbo 2.0 API, this operation is `DELETE /webhook/unsubscribe/{webhook_id}` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.

