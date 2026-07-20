# OpenQR: Update Folder

Updates an existing folder in OpenQR.

```
PUT https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenQR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "79",
  "name": "Updated folder"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "79",
    "name": "Updated folder"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | number | yes | Folder ID. Example: `79`. |
| `name` | string | yes | Folder name. Example: `Updated folder`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native OpenQR API, this operation is `POST /folders/:folder_id` (base URL `https://api.openqr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

