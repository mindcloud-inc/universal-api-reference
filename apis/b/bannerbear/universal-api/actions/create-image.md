# Bannerbear: Create Image

Creates a new image in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "string",
  "modifications": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "string",
    "modifications": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | string | yes | The Bannerbear image template UID. |
| `modifications` | list<object> | yes | Layer modifications to apply when generating the image. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | no | Webhook URL to receive the render result. |
| `transparent` | boolean | no | Render the image with a transparent background when supported. |
| `renderPdf` | boolean | no | Render a PDF instead of an image when supported. |
| `templateVersion` | number | no | Specific template version number to render. |
| `metadata` | string | no | Custom metadata to attach to the generated image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/images` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

