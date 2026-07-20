# Scrape Creators: Get Twitter Profile

Retrieves a Twitter profile from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-twitter-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-twitter-profile?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-twitter-profile?${params}`, {
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
| `handle` | string | yes | Twitter handle |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "affiliates_highlighted_label": {},
      "avatar": {},
      "business_account": {},
      "core": {},
      "creator_subscriptions_count": 1,
      "credits_remaining": 1,
      "dm_permissions": {},
      "has_hidden_subscriptions_on_profile": true,
      "highlights_info": {},
      "id": "string",
      "is_blue_verified": true,
      "legacy": {},
      "location": {},
      "privacy": {},
      "rest_id": "string",
      "success": true,
      "tipjar_settings": {},
      "verification": {},
      "verification_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__typename` | string |  |
| `affiliates_highlighted_label` | object |  |
| `avatar` | object |  |
| `business_account` | object |  |
| `core` | object |  |
| `creator_subscriptions_count` | number |  |
| `credits_remaining` | number |  |
| `dm_permissions` | object |  |
| `has_hidden_subscriptions_on_profile` | boolean |  |
| `highlights_info` | object |  |
| `id` | string |  |
| `is_blue_verified` | boolean |  |
| `legacy` | object |  |
| `location` | object |  |
| `privacy` | object |  |
| `rest_id` | string |  |
| `success` | boolean |  |
| `tipjar_settings` | object |  |
| `verification` | object |  |
| `verification_info` | object |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/twitter/profile` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-twitter-profile.md) for the provider-specific parameters and requirements.

