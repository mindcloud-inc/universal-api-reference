# Chatvolt AI: Delete/Toggle Artifact

Deletes an artifact from Chatvolt AI, or toggles its active status.

```
DELETE https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-delete?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-delete?${params}`, {
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
| `id` | string | yes |  |
| `action` | string | no | Action to perform: "delete" to remove, "toggle" to switch active status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "categoryId": "string",
      "createdAt": "string",
      "customJson": {},
      "description": "string",
      "externalUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "media": [
        "string"
      ],
      "name": "Ava Chen",
      "price": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | Category. |
| `categoryId` | string | CategoryId. |
| `createdAt` | string | CreatedAt. |
| `customJson` | object | CustomJson. |
| `description` | string | Description. |
| `externalUrl` | string | ExternalUrl. |
| `id` | string | Id. |
| `isActive` | boolean | IsActive. |
| `media` | array | Media. |
| `name` | string | Name. |
| `price` | number | Price. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `DELETE /artifacts/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-delete.md) for the provider-specific parameters and requirements.

