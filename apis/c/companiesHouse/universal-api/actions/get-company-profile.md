# Companies House: Get Company Profile

Retrieves a company profile from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile?connectionId=$CONNECTION_ID&companyNumber=00000006" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "00000006"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile?${params}`, {
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
| `companyNumber` | string | yes | The company number. Example: `00000006`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": {},
      "can_file": true,
      "company_name": "Ava Chen",
      "company_number": "string",
      "company_status": "string",
      "confirmation_statement": {},
      "date_of_creation": "string",
      "etag": "string",
      "has_been_liquidated": true,
      "has_charges": true,
      "has_insolvency_history": true,
      "has_super_secure_pscs": true,
      "jurisdiction": "string",
      "links": {},
      "registered_office_address": {},
      "sic_codes": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | object |  |
| `can_file` | boolean |  |
| `company_name` | string |  |
| `company_number` | string |  |
| `company_status` | string |  |
| `confirmation_statement` | object |  |
| `date_of_creation` | string |  |
| `etag` | string |  |
| `has_been_liquidated` | boolean |  |
| `has_charges` | boolean |  |
| `has_insolvency_history` | boolean |  |
| `has_super_secure_pscs` | boolean |  |
| `jurisdiction` | string |  |
| `links` | object |  |
| `registered_office_address` | object |  |
| `sic_codes` | array |  |
| `type` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-profile.md) for the provider-specific parameters and requirements.

