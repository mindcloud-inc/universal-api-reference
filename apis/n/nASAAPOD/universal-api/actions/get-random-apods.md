# NASA APOD: Get Random APODs



```
GET https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-random-apods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NASA APOD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-random-apods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-random-apods?${params}`, {
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
| `count` | number | no | Number of randomly selected APODs. Default: `1`. |
| `thumbs` | boolean | no | When true, NASA includes thumbnail_url for video APODs. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "copyright": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "explanation": "string",
      "hdurl": "https://example.com",
      "media_type": "string",
      "service_version": "string",
      "thumbnail_url": "https://example.com",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `copyright` | string | Optional copyright holder; present when the item is not public domain. |
| `date` | date | APOD date. |
| `explanation` | string | NASA's description of the APOD. |
| `hdurl` | string | Optional high-resolution image URL. |
| `media_type` | string | Media type, such as image or video. |
| `service_version` | string | APOD service version. |
| `thumbnail_url` | string | Optional video thumbnail URL when thumbs is requested. |
| `title` | string | APOD title. |
| `url` | string | Media URL. |

## Native endpoint

Through the native NASA APOD API, this operation is `GET /planetary/apod` (base URL `https://api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-apods.md) for the provider-specific parameters and requirements.

