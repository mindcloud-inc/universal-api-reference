# Koncile OCR: Create Folder



```
POST https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desc` | string | no | A detailed description of the folder. |
| `name` | string | yes | The folder name to create. |

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

Through the native Koncile OCR API, this operation is `POST /create_folder` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

