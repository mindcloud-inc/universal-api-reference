# Stencil: List Templates



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/list-templates?${params}`, {
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
| `projectId` | string | yes | Project ID from Stencil. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableModifications": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "self": "string",
      "signedImageBase": "string",
      "starred": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableModifications` | array<object> |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `self` | string |  |
| `signedImageBase` | string |  |
| `starred` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Stencil API, this operation is `GET /v1/projects/:project_id/templates` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

