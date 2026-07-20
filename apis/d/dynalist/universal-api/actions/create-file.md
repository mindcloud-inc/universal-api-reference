# Dynalist: Create File

Creates a new file or folder in Dynalist.

```
POST https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileType": "string",
  "parentId": "string",
  "index": "-1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileType": "string",
    "parentId": "string",
    "index": "-1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileType` | string | yes | Type of file to create: document or folder. |
| `parentId` | string | yes | ID of the parent folder. |
| `index` | number | yes | Zero-indexed destination position; use -1 for the end. Default: `-1`. |
| `title` | string | no | Optional title for the new file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "created": [
        "string"
      ],
      "results": [
        true
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |
| `created` | array<string> |  |
| `results` | array<boolean> |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /file/edit` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

