# Companies House: Search Companies Advanced

Finds companies in Companies House by advanced filters.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-advanced
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-advanced?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-advanced?${params}`, {
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
| `companyNameIncludes` | string | no | Filter results to company names containing this text. |

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

Through the native Companies House API, this operation is `GET /advanced-search/companies` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies-advanced.md) for the provider-specific parameters and requirements.

