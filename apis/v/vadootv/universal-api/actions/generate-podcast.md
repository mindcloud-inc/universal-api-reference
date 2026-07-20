# Vadootv: Generate podcast

Creates an AI podcast in Vadootv.

```
POST https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-podcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-podcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name1": "Host 1",
  "name2": "Host 2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-podcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name1": "Host 1",
    "name2": "Host 2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | URL of the blog post or PDF. Required if text is not provided. Example: `https://example.com/article-or-file.pdf`. |
| `text` | string | no | Raw text transcript or content. Required if url is not provided. Example: `Podcast source text when url is omitted`. |
| `name1` | string | yes | Name of the first speaker. Example: `Host 1`. |
| `name2` | string | yes | Name of the second speaker. Example: `Host 2`. |
| `voice1` | string | no | Voice for speaker 1. Default: `Onyx`. Example: `Onyx`. |
| `voice2` | string | no | Voice for speaker 2. Default: `Alloy`. Example: `Alloy`. |
| `language` | string | no | Language of the podcast. Default: `English`. Example: `English`. |
| `duration` | list<string> | no | Target duration code. One of: `1-2`, `2-5`. Default: `1-2`. |
| `tone` | string | no | Tone of the conversation. Default: `Friendly`. Example: `Friendly`. |
| `theme` | string | no | Caption theme when generating a video podcast. Default: `Hormozi_1`. Example: `Hormozi_1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `vid` | string | Video ID for the generated podcast output. |

## Native endpoint

Through the native Vadootv API, this operation is `POST /api/generate_podcast` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-podcast.md) for the provider-specific parameters and requirements.

