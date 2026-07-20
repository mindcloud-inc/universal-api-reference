# Hightouch: Create Model

Creates a new model in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slug": "string",
  "queryType": "string",
  "sourceId": 1,
  "isSchema": true,
  "primaryKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slug": "string",
    "queryType": "string",
    "sourceId": 1,
    "isSchema": true,
    "primaryKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The model name. |
| `slug` | string | yes | The model slug. |
| `queryType` | string | yes | The model query type. |
| `sourceId` | number | yes | The source ID the model is connected to. |
| `isSchema` | boolean | yes | Whether the model is only used to build other models. |
| `primaryKey` | string | yes | The primary key for synced query results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skipColumnQuery` | boolean | no | Whether to skip querying columns while creating the model. |

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

Through the native Hightouch API, this operation is `POST /models` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

