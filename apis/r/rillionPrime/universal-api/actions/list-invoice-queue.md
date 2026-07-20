# Rillion Prime: List Invoice Queue



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-queue?connectionId=$CONNECTION_ID&limit=25&offset=0&role=Administrator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "role": "Administrator"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-queue?${params}`, {
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
| `role` | string | yes | Path value for Role. Example: `Administrator`. |
| `headersOnly` | boolean | no | When true, returns only header rows where supported. |
| `updateQueueStatus` | boolean | no | Optional query value for UpdateQueueStatus. |
| `searchTerm` | string | no | Optional query value for SearchTerm. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /invoicequeue/role/:role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoice-queue.md) for the provider-specific parameters and requirements.

