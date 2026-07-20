# Google Slides: Get Page Thumbnail

Retrieves a page thumbnail URL from Google Slides.

```
GET https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page-thumbnail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page-thumbnail?connectionId=$CONNECTION_ID&presentationId=string&pageObjectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string",
  "pageObjectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-page-thumbnail?${params}`, {
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
| `presentationId` | string | yes | The ID of the presentation. |
| `pageObjectId` | string | yes | The object ID of the page thumbnail to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentUrl": "https://example.com",
      "height": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | The URL of the page thumbnail image. |
| `height` | number | The thumbnail height in pixels. |
| `width` | number | The thumbnail width in pixels. |

## Native endpoint

Through the native Google Slides API, this operation is `GET /v1/presentations/:presentationId/pages/:pageObjectId/thumbnail` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-thumbnail.md) for the provider-specific parameters and requirements.

