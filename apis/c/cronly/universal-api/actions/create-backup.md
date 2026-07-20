# Cronly: Create Backup



```
POST https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "serverId": "string",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "serverId": "string",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | The username on the server whose backup you want to create. |
| `serverId` | string | yes | The identifier string of the server for the backup. |
| `fileContent` | string | yes | The content of the crontab file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "server_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `server_id` | number |  |
| `updated_at` | date |  |
| `username` | string |  |

## Native endpoint

Through the native Cronly API, this operation is `POST /api/backups` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-backup.md) for the provider-specific parameters and requirements.

