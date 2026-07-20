# Uniqode: List Landing Pages

Retrieves landing pages from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-landing-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-landing-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-landing-pages?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `results[].created` | date |  |
| `results[].css_body` | string |  |
| `results[].default` | boolean |  |
| `results[].fb_pixel_event` | string |  |
| `results[].fb_pixel_id` | string |  |
| `results[].google_conversion_id` | string |  |
| `results[].html_body` | string |  |
| `results[].id` | number |  |
| `results[].kit_type` | string |  |
| `results[].maintainer` | number |  |
| `results[].markdown_body` | string |  |
| `results[].organization` | number |  |
| `results[].theme` | string |  |
| `results[].threat_active` | boolean |  |
| `results[].title` | string |  |
| `results[].updated` | date |  |
| `results[].version` | number |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /markdowncards/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-landing-pages.md) for the provider-specific parameters and requirements.

