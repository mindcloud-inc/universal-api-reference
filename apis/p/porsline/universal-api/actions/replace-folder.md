# Porsline: Replace Folder



```
PUT https://connect.mindcloud.co/v1/universal/porsline/latest/actions/replace-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/replace-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "107521",
  "name": "MindCloud Stage 3 Temp Folder Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/replace-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "107521",
    "name": "MindCloud Stage 3 Temp Folder Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | number | yes | Selected folder id. Example: `107521`. |
| `name` | string | yes | The name of the folder. Example: `MindCloud Stage 3 Temp Folder Updated`. |
| `order` | number | no | The folder order. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |

## Native endpoint

Through the native Porsline API, this operation is `PUT /api/folders/:folder_id/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-folder.md) for the provider-specific parameters and requirements.

