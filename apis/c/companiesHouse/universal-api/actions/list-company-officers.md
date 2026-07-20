# Companies House: List Company Officers

Retrieves company officers from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-officers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-officers?connectionId=$CONNECTION_ID&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-officers?${params}`, {
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
      "active_count": 1,
      "etag": "string",
      "inactive_count": 1,
      "items": [
        "string"
      ],
      "items_per_page": 1,
      "kind": "string",
      "links": {},
      "resigned_count": 1,
      "start_index": 1,
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_count` | number |  |
| `etag` | string |  |
| `inactive_count` | number |  |
| `items` | array |  |
| `items_per_page` | number |  |
| `kind` | string |  |
| `links` | object |  |
| `resigned_count` | number |  |
| `start_index` | number |  |
| `total_results` | number |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/officers` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-officers.md) for the provider-specific parameters and requirements.

