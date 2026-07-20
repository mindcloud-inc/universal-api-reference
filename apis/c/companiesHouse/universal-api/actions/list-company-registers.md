# Companies House: List Company Registers

Retrieves company registers from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-registers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-registers?connectionId=$CONNECTION_ID&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-registers?${params}`, {
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
      "company_number": "string",
      "etag": "string",
      "kind": "string",
      "links": {},
      "registers": [
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
| `company_number` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `registers` | array |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/registers` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-registers.md) for the provider-specific parameters and requirements.

