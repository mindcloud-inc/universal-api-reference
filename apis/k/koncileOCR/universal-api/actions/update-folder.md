# Koncile OCR: Update Folder



```
PUT https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folder_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folder_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desc` | string | no | Update the folder description. |
| `folder_id` | number | yes | The folder identifier to update. |
| `name` | string | no | Update the folder name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "id": 1,
      "name": "Ava Chen",
      "template_ids": [
        1
      ],
      "templates": [
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
| `desc` | string | The folder description. |
| `id` | number | The folder identifier. |
| `name` | string | The folder name. |
| `template_ids` | array<number> | Template IDs in the folder. |
| `templates` | array<object> | Templates in the folder. |

## Native endpoint

Through the native Koncile OCR API, this operation is `PUT /update_folder` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

