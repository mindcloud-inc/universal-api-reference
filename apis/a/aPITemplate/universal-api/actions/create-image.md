# API Template: Create Image

Creates an image in API Template.

```
POST https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-image', {
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
| `templateId` | string | yes | Template ID to render. |
| `outputImageType` | string | no | Return JPEG, PNG, or both. |
| `expiration` | number | no | Minutes before the generated file expires; use 0 to store permanently. |
| `cloudStorage` | number | no | Whether to upload the generated file to APITemplate cloud storage. |
| `meta` | string | no | Optional metadata string to attach to the job. |
| `overrides[]` | array<object> | no | Array of object overrides to apply to the image template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native API Template API returns.

## Native endpoint

Through the native API Template API, this operation is `POST /v2/create-image` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

