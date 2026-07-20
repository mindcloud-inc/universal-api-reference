# Picnie: Create Image Collection

Creates an image collection in Picnie from a template.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-image-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-image-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateGroupId": "3",
  "projectId": 1,
  "details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-image-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateGroupId": "3",
    "projectId": 1,
    "details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateGroupId` | number | yes | Template group ID to use for collection generation. Example: `3`. |
| `projectId` | number | yes | Project ID that will own the generated image collection. |
| `outputImageQuality` | string | no | Optional image quality: Maximum, High, Medium, or Low. Example: `High`. |
| `outputImageFormat` | string | no | Optional output format: jpg, png, gif, or webp. Example: `png`. |
| `details` | object<object> | yes | Template field values to merge into every image in the collection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `urls[]` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /create-image-collection` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-collection.md) for the provider-specific parameters and requirements.

