# Syncro: List Customers

Retrieves a list of customers from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-customers?${params}`, {
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
| `query` | string | no | General customer search text. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `businessName` | string | no |  |
| `id` | number | no |  |
| `notId` | number | no | Exclude a specific customer ID from the results. |
| `email` | string | no |  |
| `includeDisabled` | boolean | no | Include disabled customers in the results. |
| `sort` | string | no | Customer field and direction, for example firstname ASC. |
| `page` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Syncro API returns.

## Native endpoint

Through the native Syncro API, this operation is `GET /customers` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

