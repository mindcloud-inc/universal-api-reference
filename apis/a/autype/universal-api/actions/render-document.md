# Autype: Render Document

Creates a temporary document render job from JSON in Autype.

```
POST https://connect.mindcloud.co/v1/universal/autype/latest/actions/render-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autype/latest/actions/render-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "config": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autype/latest/actions/render-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "config": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | object | yes |  |
| `strict` | boolean | no | Default: `false`. |
| `webhook` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditCost": 1,
      "downloadUrl": "https://example.com",
      "error": "string",
      "filename": "Ava Chen",
      "format": "string",
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creditCost` | number |  |
| `downloadUrl` | string |  |
| `error` | string |  |
| `filename` | string |  |
| `format` | string |  |
| `jobId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Autype API, this operation is `POST /render` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-document.md) for the provider-specific parameters and requirements.

