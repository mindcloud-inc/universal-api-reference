# Companies House: List Company PSCs

Retrieves company persons with significant control from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-pscs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-pscs?connectionId=$CONNECTION_ID&companyNumber=string&itemsPerPage=string&registerView=string&startIndex=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string",
  "itemsPerPage": "string",
  "registerView": "string",
  "startIndex": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/list-company-pscs?${params}`, {
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
| `itemsPerPage` | string | yes | The number of PSC records to return per page. |
| `registerView` | string | yes | Whether to return the register view of the PSC data. |
| `startIndex` | string | yes | The zero-based index of the first PSC record to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_count": 1,
      "ceased_count": 1,
      "items": [
        "string"
      ],
      "items_per_page": 1,
      "links": {},
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
| `ceased_count` | number |  |
| `items` | array |  |
| `items_per_page` | number |  |
| `links` | object |  |
| `start_index` | number |  |
| `total_results` | number |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/persons-with-significant-control` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-pscs.md) for the provider-specific parameters and requirements.

