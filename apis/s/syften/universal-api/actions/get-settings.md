# Syften: Get Settings

Retrieves keyword alert settings from Syften.

```
GET https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syften `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "api_token": "string",
      "keywords": [
        "string"
      ],
      "options": "string",
      "rss_token": "string",
      "slack": {},
      "slacks": [
        "string"
      ],
      "twitter_keywords": [
        "string"
      ],
      "youtube_keywords": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_token` | string |  |
| `keywords` | array<string> |  |
| `options` | string |  |
| `rss_token` | string |  |
| `slack` | object |  |
| `slacks` | array<string> |  |
| `twitter_keywords` | array<string> |  |
| `youtube_keywords` | array<string> |  |

## Native endpoint

Through the native Syften API, this operation is `POST /api/0.0/settings/get` (base URL `https://syften.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings.md) for the provider-specific parameters and requirements.

