# Xano: Update API Group

Updates an existing API group in Xano.

```
PUT https://connect.mindcloud.co/v1/universal/xano/latest/actions/update-api-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xano/latest/actions/update-api-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apigroup_id": 1,
  "workspace_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xano/latest/actions/update-api-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apigroup_id": 1,
    "workspace_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apigroup_id` | number | yes | The Xano API group ID. |
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "canonical": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docs": "string",
      "guid": "string",
      "id": 1,
      "name": "Ava Chen",
      "swagger": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `canonical` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `docs` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `name` | string |  |
| `swagger` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Xano API, this operation is `PUT /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-api-group.md) for the provider-specific parameters and requirements.

