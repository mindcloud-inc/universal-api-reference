# Optform: Get Form

Retrieves a form from Optform.

```
GET https://connect.mindcloud.co/v1/universal/optform/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/get-form?connectionId=$CONNECTION_ID&id=ypo_HH12jj" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ypo_HH12jj"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optform/latest/actions/get-form?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `ypo_HH12jj`. |

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

Through the native Optform API, this operation is `GET /api/Form/:id` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

