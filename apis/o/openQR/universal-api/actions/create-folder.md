# OpenQR: Create Folder

Creates a new folder in OpenQR.

```
POST https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenQR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Demo folder"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Demo folder"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Folder name. Example: `Demo folder`. |

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

Through the native OpenQR API, this operation is `POST /folders` (base URL `https://api.openqr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

