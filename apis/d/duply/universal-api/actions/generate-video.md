# Duply: Generate Video

Creates a generated video from a Duply template.

```
POST https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "formats[]": [
    "string"
  ],
  "fill": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "formats[]": ["string"],
    "fill": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The ID of the template to generate from. |
| `formats[]` | array<string> | yes | Video output formats to generate. Duply currently documents mp4. |
| `fill` | object | yes | Template element values keyed by the element name. |
| `requestName` | string | no | Optional identifier for the generation request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Duply API, this operation is `POST /generate-video/` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video.md) for the provider-specific parameters and requirements.

