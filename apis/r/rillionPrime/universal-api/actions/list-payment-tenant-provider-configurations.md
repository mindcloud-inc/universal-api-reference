# Rillion Prime Pay: List Payment Tenant Provider Configurations



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-provider-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-provider-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-provider-configurations?${params}`, {
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
      "enablePaymentGrouping": true,
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enablePaymentGrouping` | boolean |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/configuration/tenant/provider` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-tenant-provider-configurations.md) for the provider-specific parameters and requirements.

