# deAPI: Create Text-to-Music Job

Creates a text-to-music job in deAPI.

```
POST https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-music-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-music-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/create-text-to-music-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caption` | string | no | Text description of the music to generate. |
| `duration` | string | no | Music duration in seconds. |
| `format` | string | no | Audio output format. |
| `guidanceScale` | string | no | Classifier-free guidance scale. |
| `inferenceSteps` | string | no | Number of diffusion inference steps. |
| `lyrics` | string | no | Lyrics text, or [Instrumental] for instrumental output. |
| `model` | string | no | Music model slug from List Models. |
| `seed` | string | no | Random seed. Use -1 for random. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `POST /api/v1/client/txt2music` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-music-job.md) for the provider-specific parameters and requirements.

