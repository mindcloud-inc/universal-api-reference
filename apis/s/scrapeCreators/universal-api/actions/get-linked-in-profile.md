# Scrape Creators: Get LinkedIn Profile

Retrieves a LinkedIn profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-profile?${params}`, {
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
| `url` | string | yes | LinkedIn profile URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "articles": [
        {}
      ],
      "credits_remaining": 1,
      "education": [
        {}
      ],
      "experience": [
        {}
      ],
      "followers": 1,
      "image": "string",
      "location": "string",
      "name": "Ava Chen",
      "projects": [
        {}
      ],
      "publications": [
        {}
      ],
      "recommendations": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `articles` | array<object> |  |
| `credits_remaining` | number |  |
| `education` | array<object> |  |
| `experience` | array<object> |  |
| `followers` | number |  |
| `image` | string |  |
| `location` | string |  |
| `name` | string |  |
| `projects` | array<object> |  |
| `publications` | array<object> |  |
| `recommendations` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/linkedin/profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-in-profile.md) for the provider-specific parameters and requirements.

