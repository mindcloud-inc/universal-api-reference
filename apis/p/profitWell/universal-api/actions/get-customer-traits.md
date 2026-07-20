# ProfitWell: Get Customer Traits

Retrieves customer traits from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-customer-traits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-customer-traits?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-customer-traits?${params}`, {
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
| `customerId` | string | yes | The customer ID to retrieve traits for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/customer_traits/customer/:customer_id/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-traits.md) for the provider-specific parameters and requirements.

