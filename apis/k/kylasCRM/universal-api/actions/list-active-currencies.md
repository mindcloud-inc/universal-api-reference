# Kylas CRM: List Active Currencies



```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-active-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-active-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-active-currencies?${params}`, {
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
      "active": true,
      "baseCurrency": true,
      "createdAt": "string",
      "currencyValueId": 1,
      "displayName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "tenantId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the currency is active. |
| `baseCurrency` | boolean | Whether this is the tenant base currency. |
| `createdAt` | string | UTC timestamp when the currency was created. |
| `currencyValueId` | number | Kylas master currency value ID. |
| `displayName` | string | Human-readable currency name. |
| `id` | number | Kylas currency record ID. |
| `name` | string | ISO currency code. |
| `tenantId` | number | Tenant ID that owns the currency record. |
| `updatedAt` | string | UTC timestamp when the currency was last updated. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /forex/currencies` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-currencies.md) for the provider-specific parameters and requirements.

