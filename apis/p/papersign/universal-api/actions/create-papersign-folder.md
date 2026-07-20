# Papersign: Create Papersign Folder



```
POST https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papersign/latest/actions/create-papersign-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "folder": {
          "id": 1,
          "name": "Ava Chen",
          "parent_id": 1,
          "space_id": 1
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.folder.id` | number | The unique identifier of the folder. |
| `results.folder.name` | string | The name of the folder. |
| `results.folder.parent_id` | number | The unique identifier of the parent folder. |
| `results.folder.space_id` | number | The unique identifier of the space. |
| `status` | string | Response status. |

## Native endpoint

Through the native Papersign API, this operation is `POST /papersign/folders` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-papersign-folder.md) for the provider-specific parameters and requirements.

