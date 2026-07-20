# Encodian - Sign: Delete Trigr Webhook Subscription



```
DELETE https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/delete-trigr-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/delete-trigr-webhook-subscription?connectionId=$CONNECTION_ID&tenantWebHookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenantWebHookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/delete-trigr-webhook-subscription?${params}`, {
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
| `tenantWebHookId` | number | yes | ID of the Encodian Trigr webhook subscription to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encodian - Sign API returns.

## Native endpoint

Through the native Encodian - Sign API, this operation is `DELETE /api/v1/Trigr/ManageWebHook/:tenantWebHookId` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-trigr-webhook-subscription.md) for the provider-specific parameters and requirements.

