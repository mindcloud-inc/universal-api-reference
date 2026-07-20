# Implisense: Search Companies

Finds companies in Implisense API with filters and facets.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/search-companies?${params}`, {
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
| `query` | string | no | Free-text company search query. |
| `from` | number | no | Result offset for search pagination. Default: `0`. |
| `size` | number | no | Maximum number of results to return. Default: `10`. |
| `explain` | boolean | no | Include explanation details in the search result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "city": "string",
      "explanation": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "profile": "string",
      "score": 1,
      "snippets": [
        {}
      ],
      "street": "string",
      "url": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `city` | string |  |
| `explanation` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `profile` | string |  |
| `score` | number |  |
| `snippets` | array<object> |  |
| `street` | string |  |
| `url` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `POST /search` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

