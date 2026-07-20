# Localazy: Replace Screenshot Image

Updates an existing screenshot image in a Localazy project.

```
PUT https://connect.mindcloud.co/v1/universal/localazy/latest/actions/replace-screenshot-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/replace-screenshot-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "screenshotId": "string",
  "imageData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/replace-screenshot-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "screenshotId": "string",
    "imageData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project identifier or slug. |
| `screenshotId` | string | yes | Identifier of the screenshot to replace. |
| `imageData` | string | yes | Image as a data URI, for example data:image/png;base64,... |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether the screenshot image was replaced successfully. |

## Native endpoint

Through the native Localazy API, this operation is `POST /projects/:projectId/screenshots/:screenshotId` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-screenshot-image.md) for the provider-specific parameters and requirements.

