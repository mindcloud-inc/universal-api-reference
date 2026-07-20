# Uniqode: Create Landing Page

Creates a new landing page in Uniqode.

```
POST https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-landing-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-landing-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/create-landing-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "css_body": "string",
      "default": true,
      "fb_pixel_event": "string",
      "fb_pixel_id": "string",
      "google_conversion_id": "string",
      "html_body": "string",
      "id": 1,
      "kit_type": "string",
      "maintainer": 1,
      "markdown_body": "string",
      "organization": 1,
      "theme": "string",
      "threat_active": true,
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `css_body` | string |  |
| `default` | boolean |  |
| `fb_pixel_event` | string |  |
| `fb_pixel_id` | string |  |
| `google_conversion_id` | string |  |
| `html_body` | string |  |
| `id` | number |  |
| `kit_type` | string |  |
| `maintainer` | number |  |
| `markdown_body` | string |  |
| `organization` | number |  |
| `theme` | string |  |
| `threat_active` | boolean |  |
| `title` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Uniqode API, this operation is `POST /markdowncards/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-landing-page.md) for the provider-specific parameters and requirements.

