# Zoho Sign: Create Folder

Creates a folder in Zoho Sign.

```
POST https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "data.folders": {},
  "data.folders.folderName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "data.folders": {},
    "data.folders.folderName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Zoho Sign folder payload wrapper. |
| `data.folders` | object | yes | Folder details. |
| `data.folders.folderName` | string | yes | Name of the folder to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "folders": {
        "folderId": "string",
        "folderName": "Ava Chen"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `folders` | object |  |
| `folders.folderId` | string |  |
| `folders.folderName` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `POST /folders` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

