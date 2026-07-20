# Eduzz: Get Financial Statement

Retrieves a financial statement from Eduzz using provided filters.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-financial-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-financial-statement?connectionId=$CONNECTION_ID&limit=25&offset=0&endDate=2026-03-18&startDate=2024-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "endDate": "2026-03-18",
  "startDate": "2024-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-financial-statement?${params}`, {
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
| `endDate` | string | yes | Include statement entries through this date. Example: `2026-03-18`. |
| `saleId` | string | no | Filter statement entries by sale id. |
| `startDate` | string | yes | Include statement entries from this date onward. Example: `2024-01-01`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /myeduzz/v2/financial/statement` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-financial-statement.md) for the provider-specific parameters and requirements.

