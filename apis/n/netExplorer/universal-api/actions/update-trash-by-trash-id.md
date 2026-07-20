# NetExplorer: Update Trash



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-trash-by-trash-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-trash-by-trash-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trashId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-trash-by-trash-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trashId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trashId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canDownload": true,
      "canEdit": true,
      "canRead": true,
      "canWrite": true,
      "creation": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modification": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": "string",
      "ownerId": 1,
      "parentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canDownload` | boolean |  |
| `canEdit` | boolean |  |
| `canRead` | boolean |  |
| `canWrite` | boolean |  |
| `creation` | date |  |
| `id` | number |  |
| `modification` | date |  |
| `name` | string |  |
| `owner` | string |  |
| `ownerId` | number |  |
| `parentId` | string |  |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /trash/:trashId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-trash-by-trash-id.md) for the provider-specific parameters and requirements.

