# Enrich.so: Search Leads

Finds leads in Enrich.so by search filters.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/search-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/search-leads?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/search-leads?${params}`, {
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
| `filters` | object | yes | Lead finder filter object. Default: `{"company":{"domains":["stripe.com"]}}`. |
| `page` | number | no | Page number, starting at 1. |
| `pageSize` | number | no | Results per page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `excludeFilters` | object | no | Optional filters to exclude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "firstName": "Ava",
      "insights": {},
      "lastName": "Chen",
      "linkedin": "https://example.com",
      "location": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Lead company name. |
| `firstName` | string | Lead first name. |
| `insights` | object | Lead and company insights returned by search. |
| `lastName` | string | Lead last name, potentially masked by default search results. |
| `linkedin` | string | Lead LinkedIn profile URL. |
| `location` | string | Lead location. |
| `title` | string | Lead job title. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /lead-finder/search` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-leads.md) for the provider-specific parameters and requirements.

