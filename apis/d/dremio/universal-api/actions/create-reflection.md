# Dremio: Create Reflection

Creates a new reflection in a Dremio project.

```
POST https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-reflection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-reflection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "name": "Ava Chen",
  "projectId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-reflection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "name": "Ava Chen",
    "projectId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes |  |
| `name` | string | yes |  |
| `projectId` | string | yes |  |
| `type` | string | yes |  |

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

Through the native Dremio API, this operation is `POST /projects/:project_id/reflection` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reflection.md) for the provider-specific parameters and requirements.

