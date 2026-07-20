# Eduzz: List Sales

Retrieves sales from Eduzz using the provided filters.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-sales?connectionId=$CONNECTION_ID&limit=25&offset=0&endDate=2026-03-18T23%3A59%3A59Z&startDate=2024-01-01T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "endDate": "2026-03-18T23:59:59Z",
  "startDate": "2024-01-01T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-sales?${params}`, {
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
| `affiliateId` | string | no | Filter sales by affiliate id. Example: `654321`. |
| `buyerDocument` | string | no | Filter sales by buyer document. Example: `12345678901`. |
| `buyerEmail` | string | no | Filter sales by buyer email. Example: `buyer@example.com`. |
| `contractId` | string | no | Filter sales by contract id. Example: `123456`. |
| `endDate` | string | yes | Include sales through this date. Example: `2026-03-18T23:59:59Z`. |
| `productId` | string | no | Filter sales by product id. Example: `987654`. |
| `referenceDate` | string | no | Sales date basis accepted by Eduzz. Example: `paidAt`. |
| `startDate` | string | yes | Include sales from this date onward. Example: `2024-01-01T00:00:00Z`. |
| `status` | string | no | Filter sales by status. Example: `paid`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /myeduzz/v1/sales` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

