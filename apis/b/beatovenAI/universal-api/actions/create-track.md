# Beatoven AI: Create Track

Creates a new track in Beatoven AI from a text prompt.

```
POST https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/create-track
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beatoven AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/create-track" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt.text": "5 seconds soft piano note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/create-track', {
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
| `prompt.text` | string | yes | Text prompt describing the track you want Beatoven to initialize. Default: `5 seconds soft piano note`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "tracks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `tracks` | array<string> |  |

## Native endpoint

Through the native Beatoven AI API, this operation is `POST /tracks` (base URL `https://public-api.beatoven.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-track.md) for the provider-specific parameters and requirements.

