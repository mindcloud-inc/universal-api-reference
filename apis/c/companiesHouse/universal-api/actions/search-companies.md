# Companies House: Search Companies

Finds companies in Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies?${params}`, {
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
| `q` | string | yes | The search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        "string"
      ],
      "items_per_page": 1,
      "kind": "string",
      "page_number": 1,
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
| `items` | array |  |
| `items_per_page` | number |  |
| `kind` | string |  |
| `page_number` | number |  |
| `start_index` | number |  |
| `total_results` | number |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /search/companies` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

