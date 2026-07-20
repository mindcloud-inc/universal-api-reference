# Companies House: Get Company PSC Individual

Retrieves an individual person with significant control notification from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-individual
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-individual?connectionId=$CONNECTION_ID&companyNumber=string&pscId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string",
  "pscId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-individual?${params}`, {
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
| `companyNumber` | string | yes | The company number. |
| `pscId` | string | yes | The PSC ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "ceased_on": "string",
      "country_of_residence": "string",
      "date_of_birth": {},
      "etag": "string",
      "identity_verification_details": {},
      "kind": "string",
      "links": {},
      "name": "Ava Chen",
      "name_elements": {},
      "nationality": "string",
      "natures_of_control": [
        "string"
      ],
      "notified_on": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `ceased_on` | string |  |
| `country_of_residence` | string |  |
| `date_of_birth` | object |  |
| `etag` | string |  |
| `identity_verification_details` | object |  |
| `kind` | string |  |
| `links` | object |  |
| `name` | string |  |
| `name_elements` | object |  |
| `nationality` | string |  |
| `natures_of_control` | array |  |
| `notified_on` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/persons-with-significant-control/individual/:psc_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-psc-individual.md) for the provider-specific parameters and requirements.

