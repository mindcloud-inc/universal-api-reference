# Dremio: Get Source

Retrieves a source from a Dremio project.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-source?connectionId=$CONNECTION_ID&id=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-source?${params}`, {
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
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entityType": "string",
      "id": "string",
      "name": "Ava Chen",
      "permissions": [
        {}
      ],
      "sourceChangeState": "string",
      "tag": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `createdAt` | date |  |
| `entityType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `permissions` | array<object> |  |
| `sourceChangeState` | string |  |
| `tag` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/catalog/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source.md) for the provider-specific parameters and requirements.

