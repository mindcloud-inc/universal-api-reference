# Imagior: Generate Image

Creates an image in Imagior from a template.

```
POST https://connect.mindcloud.co/v1/universal/imagior/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imagior `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imagior/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The unique ID of the design template to use for image generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "imageURL": "https://example.com",
      "message": "string",
      "requestCompletionTime": "string",
      "status": "string",
      "statusCode": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Generated image metadata. |
| `imageURL` | string | URL of the generated image. |
| `message` | string | Generation result message. |
| `requestCompletionTime` | string | Time it took to complete the request. |
| `status` | string | Indicates whether the request was successful. |
| `statusCode` | number | HTTP-style success code returned by Imagior. |
| `timestamp` | date | When the request completed. |
| `usage` | object | Credit usage details for the request. |

## Native endpoint

Through the native Imagior API, this operation is `POST /image/generate` (base URL `https://api.imagior.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

