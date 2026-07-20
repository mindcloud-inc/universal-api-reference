# Companies House: List Company Charges

Retrieves company charges from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-charges?connectionId=$CONNECTION_ID&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-charges?${params}`, {
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
      "etag": "string",
      "items": [
        "string"
      ],
      "part_satisfied_count": 1,
      "satisfied_count": 1,
      "total_count": 1,
      "unfiltered_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `items` | array |  |
| `part_satisfied_count` | number |  |
| `satisfied_count` | number |  |
| `total_count` | number |  |
| `unfiltered_count` | number |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/charges` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-charges.md) for the provider-specific parameters and requirements.

