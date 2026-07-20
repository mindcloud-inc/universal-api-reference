# Companies House: Get Registered Office Address

Retrieves a registered office address from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-registered-office-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-registered-office-address?connectionId=$CONNECTION_ID&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-registered-office-address?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_line_1": "string",
      "address_line_2": "string",
      "country": "string",
      "etag": "string",
      "kind": "string",
      "links": {},
      "locality": "string",
      "postal_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_line_1` | string |  |
| `address_line_2` | string |  |
| `country` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `locality` | string |  |
| `postal_code` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/registered-office-address` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-registered-office-address.md) for the provider-specific parameters and requirements.

