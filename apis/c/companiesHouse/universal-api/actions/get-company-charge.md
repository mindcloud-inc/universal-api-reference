# Companies House: Get Company Charge

Retrieves a company charge from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-charge?connectionId=$CONNECTION_ID&chargeId=string&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargeId": "string",
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-charge?${params}`, {
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
| `chargeId` | string | yes | The charge ID. |
| `companyNumber` | string | yes | The company number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge_number": 1,
      "classification": {},
      "created_on": "string",
      "delivered_on": "string",
      "etag": "string",
      "links": {},
      "particulars": {},
      "persons_entitled": [
        "string"
      ],
      "secured_details": {},
      "status": "string",
      "transactions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge_number` | number |  |
| `classification` | object |  |
| `created_on` | string |  |
| `delivered_on` | string |  |
| `etag` | string |  |
| `links` | object |  |
| `particulars` | object |  |
| `persons_entitled` | array |  |
| `secured_details` | object |  |
| `status` | string |  |
| `transactions` | array |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/charges/:charge_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-charge.md) for the provider-specific parameters and requirements.

