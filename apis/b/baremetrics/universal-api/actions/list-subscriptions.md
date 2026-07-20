# Baremetrics: List Subscriptions

Retrieves subscriptions from Baremetrics.

```
GET https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&sourceId=source_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sourceId": "source_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-subscriptions?${params}`, {
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
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `customerOid` | string | no | This allows you to return subscriptions for a given customer Example: `customer_1`. |
| `order` | string | no | Allows you to order subscriptions from newest to oldest `desc` or oldest to newest `asc` |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `GET /v1/:source_id/subscriptions` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

