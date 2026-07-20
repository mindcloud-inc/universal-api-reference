# Simpro: List Customer Payments



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customer-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customer-payments?connectionId=$CONNECTION_ID&companyId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-customer-payments?${params}`, {
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
| `companyId` | string | yes | The Simpro company ID. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Simpro API returns.

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/customerPayments/` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-payments.md) for the provider-specific parameters and requirements.

