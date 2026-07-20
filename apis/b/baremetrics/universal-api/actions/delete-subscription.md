# Baremetrics: Delete Subscription

Deletes a subscription from Baremetrics.

```
DELETE https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/delete-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/delete-subscription?connectionId=$CONNECTION_ID&oid=resource_1&sourceId=source_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "oid": "resource_1",
  "sourceId": "source_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/delete-subscription?${params}`, {
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
| `oid` | string | yes | Example: `resource_1`. |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `DELETE /v1/:source_id/subscriptions/:oid` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscription.md) for the provider-specific parameters and requirements.

