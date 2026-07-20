# Google Drive: Copy File

Creates a copy of a file in Google Drive.

```
POST https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/copy-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/copy-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/copy-file', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `fileId` | string | no | Default: `1cfhq1a5PyfkxSXz8b0vA2V07u8Jf2_bTBSZR-td3Jok`. |
| `mimeType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `kind` | string |  |
| `mimeType` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Google Drive API, this operation is `POST /drive/v3/files/:fileId/copy` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-file.md) for the provider-specific parameters and requirements.

