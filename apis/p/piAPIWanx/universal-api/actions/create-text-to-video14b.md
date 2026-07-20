# PiAPI/Wanx: Create Text to Video (14B)

Creates a text-to-video task in PiAPI/Wanx.

```
POST https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/create-text-to-video14b
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Wanx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/create-text-to-video14b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "A cinematic scene with natural motion and consistent detail"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/create-text-to-video14b', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "A cinematic scene with natural motion and consistent detail"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Describe the video you want WanX to generate. Example: `A cinematic scene with natural motion and consistent detail`. |
| `input.aspect_ratio` | string | no | Supported ratios are 16:9 and 9:16. PiAPI defaults to 16:9. Default: `16:9`. Example: `16:9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.negative_prompt` | string | no | Describe elements you want the model to avoid. Example: `blurry, flicker, low detail`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PiAPI/Wanx API returns.

## Native endpoint

Through the native PiAPI/Wanx API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-video14b.md) for the provider-specific parameters and requirements.

