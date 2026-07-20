# Raklet: Delete Subscription



```
DELETE https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-subscription?${params}`, {
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
| `subscriptionId` | string | yes | Raklet subscription identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raklet API returns.

## Native endpoint

Through the native Raklet API, this operation is `DELETE /organisations/:organisationId/subscriptions/:subscriptionId` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.

