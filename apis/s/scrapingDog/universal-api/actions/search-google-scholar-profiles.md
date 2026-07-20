# ScrapingDog: Search Google Scholar Profiles

Retrieves Google Scholar profiles through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar-profiles?connectionId=$CONNECTION_ID&authorsQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorsQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-scholar-profiles?${params}`, {
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
| `authorsQuery` | string | yes | Author name or query string to look up Google Scholar profiles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": "string",
        "next_page_token": "string",
        "previous": "string",
        "previous_page_token": "string"
      },
      "profiles": {
        "affiliations": "string",
        "author_id": "string",
        "cited_by": 1,
        "email": "ava@example.com",
        "interests": {
          "link": "https://example.com",
          "scrapingdog_link": "https://example.com",
          "title": "string"
        },
        "link": "https://example.com",
        "scrapingdog_link": "https://example.com",
        "thumbnail": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `pagination.next` | string |  |
| `pagination.next_page_token` | string |  |
| `pagination.previous` | string |  |
| `pagination.previous_page_token` | string |  |
| `profiles` | array<object> |  |
| `profiles.affiliations` | string |  |
| `profiles.author_id` | string |  |
| `profiles.cited_by` | number |  |
| `profiles.email` | string |  |
| `profiles.interests` | array<object> |  |
| `profiles.interests.link` | string |  |
| `profiles.interests.scrapingdog_link` | string |  |
| `profiles.interests.title` | string |  |
| `profiles.link` | string |  |
| `profiles.scrapingdog_link` | string |  |
| `profiles.thumbnail` | string |  |
| `profiles.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_scholar/profiles` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-scholar-profiles.md) for the provider-specific parameters and requirements.

