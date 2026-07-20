# Microsoft 365: Create Folder

Creates a folder in a Microsoft 365 drive.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderPath": "Documents",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderPath": "Documents",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderPath` | string | yes | Path of the parent folder relative to the drive root, such as Documents or Documents/Client Files. Example: `Documents`. |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "folder": {},
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parentReference": {},
      "size": 1,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date |  |
| `folder` | object |  |
| `id` | string |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `parentReference` | object |  |
| `size` | number |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/drive/root:/{{folderPath}}:/children` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

