# CodeQR - Link and QR Analytics: Create Tag

Creates a tag in CodeQR.

```
POST https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the tag to create. |
| `color` | string | no | The color of the tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `POST /tags` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

