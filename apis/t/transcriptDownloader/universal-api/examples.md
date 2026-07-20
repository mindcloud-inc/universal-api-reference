# Transcript Downloader Universal API Examples

These examples use the MindCloud API key and Transcript Downloader connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get YouTube Channel Profile

Retrieves a YouTube channel profile from Transcript Downloader.

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

Example response:

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

See the full [Get YouTube Channel Profile action reference](actions/get-you-tube-channel-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/transcriptDownloader/latest/actions/get-you-tube-channel-profile).

## Create Transcript with Speaker Labels

Creates a transcript with speaker labels in Transcript Downloader.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transcriptWithSpeakerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transcriptWithSpeakerId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "duration": 1,
        "language": "string",
        "message": "string",
        "transcriptsWithTimeStamps": [
          {
            "duration": 1,
            "speaker": "string",
            "start": 1,
            "text": "string"
          }
        ]
      },
      "mediaId": "string",
      "message": "string",
      "status": "string",
      "transcriptSpeakerCost": "string",
      "transcriptSpeakerId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Transcript with Speaker Labels action reference](actions/create-transcript-with-speaker-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/transcriptDownloader/latest/actions/create-transcript-with-speaker-labels).
