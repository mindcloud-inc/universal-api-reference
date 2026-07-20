# APOD: Get Random Astronomy Pictures

Retrieves random APOD entries from NASA.

```
GET https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-random-astronomy-pictures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a APOD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-random-astronomy-pictures?connectionId=$CONNECTION_ID&count=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-random-astronomy-pictures?${params}`, {
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
| `count` | number | yes | Number of random APOD images to retrieve. NASA allows positive integers up to 100. Example: `5`. |
| `thumbs` | boolean | no | Return thumbnail URLs when APOD media entries are videos. Default: `false`. |

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
| `copyright` | string | Copyright holder when the entry is not public domain. |
| `date` | date | APOD date. |
| `explanation` | string | NASA explanation text for the APOD entry. |
| `hdurl` | string | High-resolution image URL when NASA provides one. |
| `media_type` | string | Media type returned by NASA, usually image or video. |
| `service_version` | string | NASA APOD service version. |
| `thumbnail_url` | string | Video thumbnail URL when thumbs is enabled and the entry is a video. |
| `title` | string | APOD title. |
| `url` | string | Primary image or video URL. |

## Native endpoint

Through the native APOD API, this operation is `GET /planetary/apod` (base URL `https://api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-astronomy-pictures.md) for the provider-specific parameters and requirements.

