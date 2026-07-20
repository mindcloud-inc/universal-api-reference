# Documo: Upload File

Uploads a new file to Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | file | yes | File \| Required |
| `isPublic` | boolean | no | Boolean \| Makes file accessible by direct link stored in publicHref |
| `sharedWithAccount` | boolean | no | Boolean \| Make this file accessible by users across the account |
| `folderId` | string | no | Uuid \| UUID of the folder where the file will reside |
| `userId` | string | no | Uuid \| UUID of the user who owns this folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "bucket": "string",
      "bucketName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extension": "string",
      "folderId": 1,
      "id": 1,
      "isPublic": true,
      "mimeType": "string",
      "name": "Ava Chen",
      "sharedWithAccount": true,
      "size": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `bucket` | string |  |
| `bucketName` | string |  |
| `createdAt` | date |  |
| `extension` | string |  |
| `folderId` | number |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `mimeType` | string |  |
| `name` | string |  |
| `sharedWithAccount` | boolean |  |
| `size` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /files` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

