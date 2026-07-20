# Porsline: Update Folder



```
PUT https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "107521"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "107521"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | number | yes | Selected folder id. Example: `107521`. |
| `name` | string | no | The name of the folder. Example: `MindCloud Stage 3 Temp Folder Patched`. |
| `order` | number | no | The folder order. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "shared_by": {},
      "shared_with": [
        {}
      ],
      "surveys": [
        {}
      ]
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
| `shared_by` | object |  |
| `shared_with` | array<object> |  |
| `surveys` | array<object> |  |

## Native endpoint

Through the native Porsline API, this operation is `PATCH /api/folders/:folder_id/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

