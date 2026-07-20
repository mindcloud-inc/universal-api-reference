# Linkbreakers: Update a Directory

Updates an existing directory in Linkbreakers.

```
PUT https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/update-directory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the directory to update. |
| `name` | string | no | The new name of the directory. |
| `parentDirectoryId` | string | no | The parent directory ID. |
| `parentDirectoryIdDelete` | boolean | no | Remove the parent directory association. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directory": {
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "parentDirectoryId": "string",
        "path": "string",
        "updatedAt": "string",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directory` | object | Updated directory. |
| `directory.createdAt` | string |  |
| `directory.id` | string |  |
| `directory.name` | string |  |
| `directory.parentDirectoryId` | string |  |
| `directory.path` | string |  |
| `directory.updatedAt` | string |  |
| `directory.workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `PATCH /v1/directories/:id` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-directory.md) for the provider-specific parameters and requirements.

