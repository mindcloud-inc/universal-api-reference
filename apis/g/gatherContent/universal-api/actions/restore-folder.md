# GatherContent: Restore Folder

Restores a trashed folder in GatherContent.

```
PUT https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/restore-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/restore-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folder_uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/restore-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folder_uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folder_uuid` | string | yes | Folder UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "restored": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `restored` | boolean |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /folders/:folder_uuid/restore` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-folder.md) for the provider-specific parameters and requirements.

