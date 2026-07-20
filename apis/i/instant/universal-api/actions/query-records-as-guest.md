# Instant: Query Records As Guest

Retrieves records from Instant with guest permissions.

```
GET https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-guest?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/query-records-as-guest?${params}`, {
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
| `query` | object | yes | InstaQL query object to run. |
| `asGuest` | boolean | no | When true, runs the query with guest permissions. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instant API returns.

## Native endpoint

Through the native Instant API, this operation is `POST /admin/query` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-records-as-guest.md) for the provider-specific parameters and requirements.

