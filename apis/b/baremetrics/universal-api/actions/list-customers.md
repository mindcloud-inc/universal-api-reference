# Baremetrics: List Customers

Retrieves customers from Baremetrics.

```
GET https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&sourceId=source_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sourceId": "source_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/list-customers?${params}`, {
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
| `search` | string | no | Allows you to search for a customer based on: oid, email, notes and name |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `sort` | string | no | Allows you to sort the results. You can use ltv or created |
| `order` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `GET /v1/:source_id/customers` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

