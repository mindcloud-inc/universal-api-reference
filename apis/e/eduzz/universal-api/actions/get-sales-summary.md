# Eduzz: Get Sales Summary

Retrieves a sales summary from Eduzz using provided filters.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-sales-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-sales-summary?connectionId=$CONNECTION_ID&endDate=2026-03-18&startDate=2024-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-03-18",
  "startDate": "2024-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-sales-summary?${params}`, {
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
| `affiliateId` | string | no | Filter summary by affiliate id. |
| `contractId` | string | no | Filter summary by contract id. |
| `endDate` | string | yes | Include sales through this date. Example: `2026-03-18`. |
| `productId` | string | no | Filter summary by product id. |
| `startDate` | string | yes | Include sales from this date onward. Example: `2024-01-01`. |
| `status` | string | no | Filter summary by sale status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /myeduzz/v1/sales/summary` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-summary.md) for the provider-specific parameters and requirements.

