# ContactOut: Search Companies

Finds companies in ContactOut using company search filters.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-companies?${params}`, {
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
| `domain` | string | no | Company domain to search. |
| `name` | string | no | Company name to search. |
| `page` | string | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": "string",
      "message": "string",
      "metadata": {
        "page": 1,
        "page_size": 1,
        "total_results": 1
      },
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | string |  |
| `message` | string |  |
| `metadata.page` | number |  |
| `metadata.page_size` | number |  |
| `metadata.total_results` | number |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/company/search` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

