# Scrape Creators: Get LinkedIn Company Page

Retrieves a LinkedIn company page from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-company-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-company-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-linked-in-company-page?${params}`, {
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
| `url` | string | yes | LinkedIn company URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverImage": "string",
      "credits_remaining": 1,
      "description": "string",
      "employeeCount": 1,
      "employees": [
        {}
      ],
      "followers": 1,
      "founded": 1,
      "funding": {},
      "handle": "string",
      "headquarters": "string",
      "id": 1,
      "industry": "string",
      "location": {},
      "logo": "string",
      "name": "Ava Chen",
      "paginationToken": "string",
      "posts": [
        {}
      ],
      "similarPages": [
        {}
      ],
      "size": "string",
      "slogan": "string",
      "specialties": [
        "string"
      ],
      "success": true,
      "type": "string",
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverImage` | string |  |
| `credits_remaining` | number |  |
| `description` | string |  |
| `employeeCount` | number |  |
| `employees` | array<object> |  |
| `followers` | number |  |
| `founded` | number |  |
| `funding` | object |  |
| `handle` | string |  |
| `headquarters` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `location` | object |  |
| `logo` | string |  |
| `name` | string |  |
| `paginationToken` | string |  |
| `posts` | array<object> |  |
| `similarPages` | array<object> |  |
| `size` | string |  |
| `slogan` | string |  |
| `specialties` | array<string> |  |
| `success` | boolean |  |
| `type` | string |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/linkedin/company` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-in-company-page.md) for the provider-specific parameters and requirements.

