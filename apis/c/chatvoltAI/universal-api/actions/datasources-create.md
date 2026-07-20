# Chatvolt AI: Create Datasource

Creates a datasource in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "type": "string",
  "datastoreId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "type": "string",
    "datastoreId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | File for multipart/form-data requests. |
| `fileName` | string | no | Optional name for the uploaded file. If not provided, the original file name will be used. |
| `type` | string | yes | Type for multipart/form-data requests. |
| `datastoreId` | string | yes | DatastoreId for multipart/form-data requests. |
| `custom_id` | string | no | Optional custom ID, useful for multi-tenant configurations to filter data later. |
| `name` | string | no | Name for application/json requests. |
| `datasourceText` | string | no | Textual content of the data source (used for `file` and `qa` types when `isUpdateText` is true). |
| `id` | string | no | Optional ID of the existing datasource for update (upsert). If provided, the corresponding datasource will be updated; otherwise, a new one will be created. |
| `config` | object | no | Config for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "groupId": "string",
      "id": "string",
      "lastSynch": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | Config. |
| `createdAt` | string | CreatedAt. |
| `groupId` | string | GroupId. |
| `id` | string | Id. |
| `lastSynch` | string | LastSynch. |
| `name` | string | Name. |
| `status` | string | Status. |
| `type` | string | Type. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /datasources` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datasources-create.md) for the provider-specific parameters and requirements.

