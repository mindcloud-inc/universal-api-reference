# Tomba: Search Companies

Finds companies in Tomba by search filters.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/search-companies?${params}`, {
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
| `query` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no |  |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {
          "country": "string",
          "description": "string",
          "industry": "string",
          "linkedin_url": "https://example.com",
          "name": "Ava Chen",
          "total_emails": 1,
          "website_url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies[].country` | string |  |
| `companies[].description` | string |  |
| `companies[].industry` | string |  |
| `companies[].linkedin_url` | string |  |
| `companies[].name` | string |  |
| `companies[].total_emails` | number |  |
| `companies[].website_url` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `POST /reveal/search` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

