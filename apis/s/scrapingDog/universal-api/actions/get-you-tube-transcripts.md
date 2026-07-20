# ScrapingDog: Get YouTube Transcripts

Retrieves YouTube transcripts through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-you-tube-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-you-tube-transcripts?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-you-tube-transcripts?${params}`, {
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
| `videoId` | string | yes | YouTube video identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transcripts": {
        "duration": 1,
        "start": 1,
        "text": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transcripts` | array<object> |  |
| `transcripts.duration` | number |  |
| `transcripts.start` | number |  |
| `transcripts.text` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /youtube/transcripts` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-you-tube-transcripts.md) for the provider-specific parameters and requirements.

