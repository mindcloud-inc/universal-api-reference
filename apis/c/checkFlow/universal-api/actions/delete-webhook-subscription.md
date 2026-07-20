# CheckFlow: Delete Webhook Subscription



```
DELETE https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-webhook-subscription?connectionId=$CONNECTION_ID&subscriptionId=5756c4ba-7fec-4280-9011-94a2b5bbdb12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "5756c4ba-7fec-4280-9011-94a2b5bbdb12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/delete-webhook-subscription?${params}`, {
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
| `subscriptionId` | string | yes | The id of the web hook subscription you want to delete. Example: `5756c4ba-7fec-4280-9011-94a2b5bbdb12`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `DELETE /api/web-hook/unsubscribe` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-subscription.md) for the provider-specific parameters and requirements.

