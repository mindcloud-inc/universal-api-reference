# Optform: Update Form

Updates an existing form in Optform.

```
PUT https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "ypo_HH12jj",
  "name": "Ava Chen",
  "workspaceId": "string",
  "tenantId": "string",
  "userId": "string",
  "type": "pro-form",
  "design": {},
  "settings": {},
  "share": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "ypo_HH12jj",
    "name": "Ava Chen",
    "workspaceId": "string",
    "tenantId": "string",
    "userId": "string",
    "type": "pro-form",
    "design": {},
    "settings": {},
    "share": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `ypo_HH12jj`. |
| `name` | string | yes |  |
| `workspaceId` | string | yes |  |
| `tenantId` | string | yes |  |
| `userId` | string | yes |  |
| `type` | string | yes | Default: `pro-form`. |
| `design` | object | yes |  |
| `settings` | object | yes |  |
| `share` | object | yes |  |

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

Through the native Optform API, this operation is `PUT /api/Form` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

