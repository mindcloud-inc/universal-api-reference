# Longreads: Get Web App Manifest

Retrieves the Longreads web app manifest.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-web-app-manifest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-web-app-manifest?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-web-app-manifest?${params}`, {
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
      "background_color": "string",
      "dir": "string",
      "display": "string",
      "icons": [
        {}
      ],
      "lang": "string",
      "name": "Ava Chen",
      "short_name": "Ava Chen",
      "start_url": "https://example.com",
      "theme_color": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background_color` | string |  |
| `dir` | string |  |
| `display` | string |  |
| `icons` | array<object> |  |
| `lang` | string |  |
| `name` | string |  |
| `short_name` | string |  |
| `start_url` | string |  |
| `theme_color` | string |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/web-app-manifest` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-app-manifest.md) for the provider-specific parameters and requirements.

