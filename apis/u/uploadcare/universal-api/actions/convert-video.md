# Uploadcare: Convert Video

Creates a video conversion in Uploadcare.

```
POST https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/convert-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/convert-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paths[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/convert-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paths[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paths[]` | array<string> | yes | List of source video paths to convert. |
| `store` | string | no | Whether to store converted video outputs permanently. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "problems": {},
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `problems` | object | Conversion problems keyed by source when present. |
| `result` | array<object> | Queued video conversion results, including token and converted file UUID. |

## Native endpoint

Through the native Uploadcare API, this operation is `POST /convert/video/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-video.md) for the provider-specific parameters and requirements.

