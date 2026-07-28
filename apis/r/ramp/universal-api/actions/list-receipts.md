# Ramp: List Receipts



```
GET https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ramp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-receipts?${params}`, {
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
| `foo` | string | no |  |
| `createdAfter` | date | no |  |
| `createdBefore` | date | no |  |
| `fromDate` | date | no |  |
| `toDate` | date | no |  |
| `transactionId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ramp API returns.

## Native endpoint

Through the native Ramp API, this operation is `GET receipts` (base URL `https://api.ramp.com/developer/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipts.md) for the provider-specific parameters and requirements.

