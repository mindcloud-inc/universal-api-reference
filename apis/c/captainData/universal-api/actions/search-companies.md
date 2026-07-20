# Captain Data: Search Companies

Finds companies in Captain Data by Sales Navigator query.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-companies?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-companies?${params}`, {
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
| `query` | string | yes | Sales Navigator company search query copied from the LinkedIn search URL. |
| `cursor` | string | no | Pagination cursor from the X-Pagination-Next response header. |
| `pageSize` | number | no | Captain Data fixed company-search page size. Leave at the documented default. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "company_name": "Ava Chen",
      "description": "string",
      "li_company_id": 1,
      "li_company_url": "https://example.com",
      "number_employees": "string",
      "sn_company_url": "https://example.com",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `company_name` | string |  |
| `description` | string |  |
| `li_company_id` | number |  |
| `li_company_url` | string |  |
| `number_employees` | string |  |
| `sn_company_url` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /companies/search` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

