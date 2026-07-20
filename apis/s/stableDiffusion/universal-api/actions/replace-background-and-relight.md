# Stable Diffusion: Replace Background And Relight

Replaces an image background and relights the subject in Stable Diffusion.

```
POST https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/replace-background-and-relight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stable Diffusion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/replace-background-and-relight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject_image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/replace-background-and-relight', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject_image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject_image` | string | yes | Foreground subject image to relight against a generated or referenced background. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish_reason": "string",
      "image": "string",
      "seed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish_reason` | string |  |
| `image` | string |  |
| `seed` | number |  |

## Native endpoint

Through the native Stable Diffusion API, this operation is `POST /v2beta/stable-image/edit/replace-background-and-relight` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-background-and-relight.md) for the provider-specific parameters and requirements.

