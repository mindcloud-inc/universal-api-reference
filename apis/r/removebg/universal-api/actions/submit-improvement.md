# Remove.bg: Submit Improvement

Creates an improvement submission in Remove.bg.

```
POST https://connect.mindcloud.co/v1/universal/removebg/latest/actions/submit-improvement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remove.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/submit-improvement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/removebg/latest/actions/submit-improvement', {
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
| `imageUrl` | string | no | Source image URL. Provide exactly one image source. |
| `imageFilename` | string | no | Filename to use when the submitted image data does not include one. |
| `tag` | string | no | Group related submissions with a shared tag. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageFileB64` | string | no | Base64-encoded source image. Provide exactly one image source. |

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

Through the native Remove.bg API, this operation is `POST /improve` (base URL `https://api.remove.bg/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-improvement.md) for the provider-specific parameters and requirements.

