# Rillion Prime: List Payment Supplier Statuses



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-supplier-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-supplier-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-supplier-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /payment/supplier/status` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-supplier-statuses.md) for the provider-specific parameters and requirements.

