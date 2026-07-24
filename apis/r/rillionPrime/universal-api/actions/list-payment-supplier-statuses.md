# Rillion Prime Pay: List Payment Supplier Statuses



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-supplier-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

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

```json
{
  "success": true,
  "data": [
    {
      "detailsRejectedCount": 1,
      "pendingApprovalCount": 1,
      "remitAddressNeededCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detailsRejectedCount` | number |  |
| `pendingApprovalCount` | number |  |
| `remitAddressNeededCount` | number |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/supplier/status` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-supplier-statuses.md) for the provider-specific parameters and requirements.

