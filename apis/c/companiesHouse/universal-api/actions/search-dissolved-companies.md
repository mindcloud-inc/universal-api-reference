# Companies House: Search Dissolved Companies

Finds dissolved companies in Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-dissolved-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-dissolved-companies?connectionId=$CONNECTION_ID&q=string&searchType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string",
  "searchType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-dissolved-companies?${params}`, {
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
| `searchType` | string | yes | The dissolved company search type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "hits": 1,
      "items": [
        "string"
      ],
      "kind": "string",
      "top_hit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `hits` | number |  |
| `items` | array |  |
| `kind` | string |  |
| `top_hit` | object |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /dissolved-search/companies` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-dissolved-companies.md) for the provider-specific parameters and requirements.

