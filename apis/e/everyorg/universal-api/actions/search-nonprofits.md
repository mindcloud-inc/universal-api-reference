# Every.org: Search Nonprofits

Finds nonprofits in Every.org by search term.

```
GET https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/search-nonprofits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/search-nonprofits?connectionId=$CONNECTION_ID&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/search-nonprofits?${params}`, {
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
| `causes` | string | no | Comma-separated causes to OR-filter search results. |
| `searchTerm` | string | yes | Search term to match nonprofit names and metadata. |
| `take` | number | no | Maximum number of results to return. Maximum 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "donationsEnabled": true,
      "ein": "string",
      "hasAdmin": true,
      "location": "string",
      "matchedTerms": [
        "string"
      ],
      "name": "Ava Chen",
      "profileUrl": "https://example.com",
      "slug": "string",
      "tags": [
        "string"
      ],
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `donationsEnabled` | boolean |  |
| `ein` | string |  |
| `hasAdmin` | boolean |  |
| `location` | string |  |
| `matchedTerms[]` | string |  |
| `name` | string |  |
| `profileUrl` | string |  |
| `slug` | string |  |
| `tags[]` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Every.org API, this operation is `GET /search/:searchTerm` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-nonprofits.md) for the provider-specific parameters and requirements.

