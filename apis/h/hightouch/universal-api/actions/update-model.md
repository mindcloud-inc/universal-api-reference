# Hightouch: Update Model

Updates an existing model in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | number | yes | The model ID. |
| `name` | string | no | The model name. |
| `primaryKey` | string | no | The primary key for synced query results. |
| `isSchema` | boolean | no | Whether the model is only used to build other models. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "isSchema": true,
      "name": "Ava Chen",
      "primaryKey": "string",
      "queryType": "string",
      "slug": "string",
      "sourceId": 1,
      "syncs": [
        1
      ],
      "tags": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Model description. |
| `id` | number | Model ID. |
| `isSchema` | boolean | Whether this model is used as a schema. |
| `name` | string | Model name. |
| `primaryKey` | string | Model primary key. |
| `queryType` | string | Model query type. |
| `slug` | string | Model slug. |
| `sourceId` | number | Source ID. |
| `syncs` | array<number> | Sync IDs using this model. |
| `tags` | object | Model tags. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `PATCH /models/{modelId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model.md) for the provider-specific parameters and requirements.

