# AXL: Get Partner Transactions



```
GET https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-partner-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AXL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-partner-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-partner-transactions?${params}`, {
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
| `fields` | string | no | Fields to return using AXL field-selection syntax, for example {id,name} Default: `{id,createdDate,updatedDate}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AXL API returns.

## Native endpoint

Through the native AXL API, this operation is `GET /partnership/transaction` (base URL `https://app.axl.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-partner-transactions.md) for the provider-specific parameters and requirements.

