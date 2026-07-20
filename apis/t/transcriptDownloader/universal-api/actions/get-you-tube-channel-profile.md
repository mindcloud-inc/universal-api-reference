# Transcript Downloader: Get YouTube Channel Profile

Retrieves a YouTube channel profile from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-channel-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-channel-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-channel-profile?${params}`, {
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
| `url` | string | yes | The YouTube channel URL. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": "string",
      "country": "string",
      "creationDate": "string",
      "description": "string",
      "download": {
        "cost": "string",
        "createdAt": "string",
        "id": "string",
        "response": "string",
        "status": "string",
        "type": "string",
        "youtubeVideoId": "string"
      },
      "source": "string",
      "status": "string",
      "subscriberCount": 1,
      "thumbnail": "string",
      "title": "string",
      "totalMedia": 1,
      "totalViews": 1,
      "url": "https://example.com",
      "videos": [
        {
          "duration": 1,
          "publishedAt": "string",
          "thumbnail": "string",
          "title": "string",
          "youtubeId": "string"
        }
      ],
      "youtubeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | string |  |
| `country` | string |  |
| `creationDate` | string |  |
| `description` | string |  |
| `download` | object |  |
| `download.cost` | string |  |
| `download.createdAt` | string |  |
| `download.id` | string |  |
| `download.response` | string |  |
| `download.status` | string |  |
| `download.type` | string |  |
| `download.youtubeVideoId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `subscriberCount` | number |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `totalMedia` | number |  |
| `totalViews` | number |  |
| `url` | string |  |
| `videos` | array<object> |  |
| `videos[].duration` | number |  |
| `videos[].publishedAt` | string |  |
| `videos[].thumbnail` | string |  |
| `videos[].title` | string |  |
| `videos[].youtubeId` | string |  |
| `youtubeId` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/channel/profile` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-you-tube-channel-profile.md) for the provider-specific parameters and requirements.

