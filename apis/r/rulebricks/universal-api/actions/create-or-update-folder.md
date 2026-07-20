# Rulebricks: Create or Update Folder

Creates or updates a rule folder in Rulebricks.

```
POST https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-or-update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-or-update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-or-update-folder', {
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
| `description` | string | no | Description of the folder |
| `name` | string | yes | Name of the folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Folder description |
| `id` | string | Folder ID |
| `name` | string | Folder name |

## Native endpoint

Through the native Rulebricks API, this operation is `POST /admin/folders` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-folder.md) for the provider-specific parameters and requirements.

