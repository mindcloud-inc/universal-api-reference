# Dremio: Update Reflection

Updates an existing reflection in a Dremio project.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-reflection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-reflection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "projectId": "string",
  "reflection": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-reflection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "projectId": "string",
    "reflection": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `projectId` | string | yes |  |
| `reflection` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasetId": "string",
      "datasetName": "Ava Chen",
      "enabled": true,
      "entityType": "string",
      "id": "string",
      "name": "Ava Chen",
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
| `datasetId` | string |  |
| `datasetName` | string |  |
| `enabled` | boolean |  |
| `entityType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tag` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /projects/:project_id/reflection/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reflection.md) for the provider-specific parameters and requirements.

