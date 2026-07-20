# SharpAPI: Generate Seo Social Media Tags

Creates SEO and social media tags in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-seo-social-media-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-seo-social-media-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Red Bull'\''s Max Verstappen says this weekend'\''s Las Vegas Grand Prix is 99% show and 1% sporting event."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-seo-social-media-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Red Bull's Max Verstappen says this weekend's Las Vegas Grand Prix is 99% show and 1% sporting event."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide the content to generate SEO tags. Example: `Red Bull's Max Verstappen says this weekend's Las Vegas Grand Prix is 99% show and 1% sporting event.`. |
| `voiceTone` | string | no | Specify the voice tone of the output. It can be adjectives like funny or joyous, or even the name of a famous writer. Example: `joyous`. |
| `language` | string | no | Specify the language of the output, defaults to English. Example: `English`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Provider job identifier for the submitted AI job. |
| `statusUrl` | string | Provider status URL for polling the AI job result. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /seo/generate_tags` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-seo-social-media-tags.md) for the provider-specific parameters and requirements.

