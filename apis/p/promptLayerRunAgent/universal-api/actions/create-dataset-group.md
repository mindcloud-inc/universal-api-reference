# PromptLayer Run Agent: Create Dataset Group

Creates a new dataset group in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Stage 3 Dataset Group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-dataset-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Stage 3 Dataset Group"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the dataset group. Must be unique within the workspace. Example: `MindCloud Stage 3 Dataset Group`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | no | Workspace ID. Defaults to the workspace associated with the API key. Example: `58624`. |
| `folderId` | number | no | Optional folder ID to create the dataset group inside. Example: `17`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataset": {},
      "dataset_group": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset` | object |  |
| `dataset_group` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/dataset-groups` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-group.md) for the provider-specific parameters and requirements.

