# Discourse: Get Site Basic Info

Retrieves basic site information from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-site-basic-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-site-basic-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-site-basic-info?${params}`, {
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
      "apple_touch_icon_url": "https://example.com",
      "description": "string",
      "favicon_url": "https://example.com",
      "header_background_color": "string",
      "header_primary_color": "string",
      "include_in_discourse_discover": true,
      "locale": "string",
      "login_required": true,
      "logo_small_url": "https://example.com",
      "logo_url": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apple_touch_icon_url` | string |  |
| `description` | string |  |
| `favicon_url` | string |  |
| `header_background_color` | string |  |
| `header_primary_color` | string |  |
| `include_in_discourse_discover` | boolean |  |
| `locale` | string |  |
| `login_required` | boolean |  |
| `logo_small_url` | string |  |
| `logo_url` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /site/basic-info.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-basic-info.md) for the provider-specific parameters and requirements.

