# Vadootv: Generate character image

Creates a character image in Vadootv.

```
POST https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-character-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-character-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "prompt": "A close-up portrait with dramatic lighting",
  "ratio": "1:1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/generate-character-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "prompt": "A close-up portrait with dramatic lighting",
    "ratio": "1:1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The AI character ID to use as a base. Example: `1`. |
| `prompt` | string | yes | Description of the scene or pose to generate. Example: `A close-up portrait with dramatic lighting`. |
| `ratio` | list<string> | yes | Output image ratio. One of: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. Default: `1:1`. |

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
| `id` | string | Generated character image request ID. |

## Native endpoint

Through the native Vadootv API, this operation is `POST /api/generate_character_image` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-character-image.md) for the provider-specific parameters and requirements.

