# Scrape Creators: Get Snapchat User Profile

Retrieves a Snapchat user profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-snapchat-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-snapchat-user-profile?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-snapchat-user-profile?${params}`, {
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
| `handle` | string | yes | Snapchat handle |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "curatedHighlights": [
        {}
      ],
      "spotlightHighlights": [
        {}
      ],
      "spotlightStoryMetadata": [
        {}
      ],
      "story": {},
      "success": true,
      "userProfile": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `curatedHighlights` | array<object> |  |
| `spotlightHighlights` | array<object> |  |
| `spotlightStoryMetadata` | array<object> |  |
| `story` | object |  |
| `success` | boolean |  |
| `userProfile` | object |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/snapchat/profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-snapchat-user-profile.md) for the provider-specific parameters and requirements.

