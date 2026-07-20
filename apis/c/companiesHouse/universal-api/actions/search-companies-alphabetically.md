# Companies House: Search Companies Alphabetically

Finds companies in Companies House alphabetically.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-alphabetically
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-alphabetically?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/search-companies-alphabetically?${params}`, {
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
| `items` | array |  |
| `kind` | string |  |
| `top_hit` | object |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /alphabetical-search/companies` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies-alphabetically.md) for the provider-specific parameters and requirements.

