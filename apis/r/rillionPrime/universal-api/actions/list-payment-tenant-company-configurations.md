# Rillion Prime Pay: List Payment Tenant Company Configurations



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-company-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-company-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-tenant-company-configurations?${params}`, {
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
      "tenantCompanies": [
        {
          "company": "string",
          "companyId": "string",
          "configuration": {
            "bankAccountIdentifier": 1,
            "buyerId": "string",
            "buyerName": "Ava Chen",
            "companyId": "string",
            "oldBuyerId": {},
            "primeBuyerId": {},
            "startDate": "string"
          },
          "name": "Ava Chen",
          "tenantId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tenantCompanies[].company` | string |  |
| `tenantCompanies[].companyId` | string |  |
| `tenantCompanies[].configuration.bankAccountIdentifier` | number |  |
| `tenantCompanies[].configuration.buyerId` | string |  |
| `tenantCompanies[].configuration.buyerName` | string |  |
| `tenantCompanies[].configuration.companyId` | string |  |
| `tenantCompanies[].configuration.oldBuyerId` | object |  |
| `tenantCompanies[].configuration.primeBuyerId` | object |  |
| `tenantCompanies[].configuration.startDate` | string |  |
| `tenantCompanies[].name` | string |  |
| `tenantCompanies[].tenantId` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/configuration/tenant/company` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-tenant-company-configurations.md) for the provider-specific parameters and requirements.

