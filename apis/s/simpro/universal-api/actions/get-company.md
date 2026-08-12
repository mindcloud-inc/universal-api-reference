# Simpro: Get Company



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-company?${params}`, {
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
| `companyId` | number | yes | The Simpro company ID. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "line1": "string",
        "line2": "string"
      },
      "banking": {
        "accountName": "Ava Chen",
        "accountNo": "string",
        "bank": "string",
        "branchCode": "string",
        "iban": "string",
        "routingNo": "string",
        "swiftCode": "string"
      },
      "billingAddress": {
        "line1": "string",
        "line2": "string"
      },
      "cISCertNo": "string",
      "companyNo": "string",
      "country": "string",
      "currency": "string",
      "dateModified": "string",
      "defaultCostCenter": {},
      "defaultLanguage": "string",
      "ein": "string",
      "email": "ava@example.com",
      "employerTaxRefNo": "string",
      "fax": "string",
      "id": 1,
      "licence": "string",
      "multiCompanyColor": {},
      "multiCompanyLabel": {},
      "name": "Ava Chen",
      "phone": "string",
      "scheduleFormat": 1,
      "singleCostCenterMode": true,
      "taxName": "Ava Chen",
      "template": true,
      "timezone": "string",
      "timezoneOffset": "string",
      "uIDateFormat": "string",
      "uITimeFormat": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.line1` | string |  |
| `address.line2` | string |  |
| `banking.accountName` | string |  |
| `banking.accountNo` | string |  |
| `banking.bank` | string |  |
| `banking.branchCode` | string |  |
| `banking.iban` | string |  |
| `banking.routingNo` | string |  |
| `banking.swiftCode` | string |  |
| `billingAddress.line1` | string |  |
| `billingAddress.line2` | string |  |
| `cISCertNo` | string |  |
| `companyNo` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `dateModified` | string |  |
| `defaultCostCenter` | object |  |
| `defaultLanguage` | string |  |
| `ein` | string |  |
| `email` | string |  |
| `employerTaxRefNo` | string |  |
| `fax` | string |  |
| `id` | number |  |
| `licence` | string |  |
| `multiCompanyColor` | object |  |
| `multiCompanyLabel` | object |  |
| `name` | string |  |
| `phone` | string |  |
| `scheduleFormat` | number |  |
| `singleCostCenterMode` | boolean |  |
| `taxName` | string |  |
| `template` | boolean |  |
| `timezone` | string |  |
| `timezoneOffset` | string |  |
| `uIDateFormat` | string |  |
| `uITimeFormat` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId` (base URL `{{credentials.buildUrl}}/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

