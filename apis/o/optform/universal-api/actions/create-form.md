# Optform: Create Form

Creates a new form in Optform.

```
POST https://connect.mindcloud.co/v1/universal/optform/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/optform/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Customer Feedback Form",
  "workspaceId": "4ff18535-b33d-4729-999a-85b7eb080530",
  "tenantId": "f8c2f5a9-f3e4-491d-9ea8-f0535a0a38fa",
  "userId": "0e79ab5c-6229-4948-904e-dd2bcabc3dc2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/optform/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Customer Feedback Form",
    "workspaceId": "4ff18535-b33d-4729-999a-85b7eb080530",
    "tenantId": "f8c2f5a9-f3e4-491d-9ea8-f0535a0a38fa",
    "userId": "0e79ab5c-6229-4948-904e-dd2bcabc3dc2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Example: `Customer Feedback Form`. |
| `workspaceId` | string | yes | Example: `4ff18535-b33d-4729-999a-85b7eb080530`. |
| `tenantId` | string | yes | Example: `f8c2f5a9-f3e4-491d-9ea8-f0535a0a38fa`. |
| `userId` | string | yes | Example: `0e79ab5c-6229-4948-904e-dd2bcabc3dc2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buttonText": "string",
      "content": "string",
      "coverImageUrl": "https://example.com",
      "description": "string",
      "design": {},
      "designSettings": "string",
      "Etag": "string",
      "id": "string",
      "lastModifiedDateTime": "string",
      "name": "Ava Chen",
      "quiz": "string",
      "settings": {},
      "share": {},
      "status": "string",
      "subtitle": "string",
      "tagline": "string",
      "tenantId": "string",
      "textAlign": "string",
      "title": "string",
      "type": "string",
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buttonText` | string |  |
| `content` | string |  |
| `coverImageUrl` | string |  |
| `description` | string |  |
| `design` | object |  |
| `designSettings` | string |  |
| `Etag` | string |  |
| `id` | string |  |
| `lastModifiedDateTime` | string |  |
| `name` | string |  |
| `quiz` | string |  |
| `settings` | object |  |
| `share` | object |  |
| `status` | string |  |
| `subtitle` | string |  |
| `tagline` | string |  |
| `tenantId` | string |  |
| `textAlign` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Optform API, this operation is `POST /api/Form` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

