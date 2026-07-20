# Lusha Connect: Search Prospecting Companies

Finds prospecting companies in Lusha Connect by filters.

```
GET https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lusha Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-companies?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-companies?${params}`, {
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
| `pages` | object | no | Pagination settings for the prospecting company search. Lusha requires size to be at least 10. |
| `filters` | object | yes | Prospecting company filters object following the official Lusha schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing": {},
      "currentPage": 1,
      "data": [
        {}
      ],
      "pageLength": 1,
      "requestId": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing` | object | Billing metadata for returned results. |
| `currentPage` | number | Current page index returned by Lusha. |
| `data` | array<object> | Matched company summaries. |
| `pageLength` | number | Number of results in the current page. |
| `requestId` | string | Lusha request identifier for the search. |
| `totalResults` | number | Total matching companies. |

## Native endpoint

Through the native Lusha Connect API, this operation is `POST /prospecting/company/search` (base URL `https://api.lusha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-prospecting-companies.md) for the provider-specific parameters and requirements.

