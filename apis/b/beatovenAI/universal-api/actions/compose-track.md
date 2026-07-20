# Beatoven AI: Compose Track

Starts track composition in Beatoven AI from a text prompt.

```
POST https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/compose-track
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beatoven AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/compose-track" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt.text": "5 seconds soft piano note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/compose-track', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt.text": "5 seconds soft piano note"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt.text` | string | yes | Text prompt describing the track you want Beatoven to compose. Default: `5 seconds soft piano note`. |
| `format` | string | no | Audio format for the generated track. Supported values are mp3, aac, and wav. One of: `0`, `1`, `2`. Default: `wav`. |
| `looping` | boolean | no | Set to true to increase looping in the generated track. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "task_id": "string",
      "track_id": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `task_id` | string |  |
| `track_id` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Beatoven AI API, this operation is `POST /tracks/compose` (base URL `https://public-api.beatoven.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compose-track.md) for the provider-specific parameters and requirements.

