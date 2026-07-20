# Column: List Wire Transfers



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/list-wire-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-wire-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-wire-transfers?${params}`, {
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
| `bankAccountId` | string | no | Filter wire transfers associated with this bank account. |
| `counterpartyId` | string | no | Filter wire transfers associated with this counterparty. |
| `status` | string | no | Filter wire transfers by status. |
| `isIncoming` | boolean | no | Whether to return incoming or outgoing wire transfers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `GET /transfers/wire` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wire-transfers.md) for the provider-specific parameters and requirements.

