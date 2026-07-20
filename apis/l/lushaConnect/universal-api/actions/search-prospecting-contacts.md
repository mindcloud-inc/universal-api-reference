# Lusha Connect: Search Prospecting Contacts

Finds prospecting contacts in Lusha Connect by filters.

```
GET https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lusha Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-contacts?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-prospecting-contacts?${params}`, {
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
| `pages` | object | no | Pagination settings for the prospecting contact search. Lusha requires size to be at least 10. |
| `filters` | object | yes | Prospecting contact and company filters object following the official Lusha schema. |

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
| `data` | array<object> | Matched contact summaries. |
| `pageLength` | number | Number of results in the current page. |
| `requestId` | string | Lusha request identifier for the search. |
| `totalResults` | number | Total matching contacts. |

## Native endpoint

Through the native Lusha Connect API, this operation is `POST /prospecting/contact/search` (base URL `https://api.lusha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-prospecting-contacts.md) for the provider-specific parameters and requirements.

