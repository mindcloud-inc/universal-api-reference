# Workiom: Update View

Updates an existing view in your Workiom workspace.

```
PUT https://connect.mindcloud.co/v1/universal/workiom/latest/actions/update-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/update-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiom/latest/actions/update-view', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibility": "string",
      "autoCollapseEnabled": true,
      "creationTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "isDefault": true,
      "isFieldsEditable": true,
      "lastModificationTime": "2026-05-07T12:00:00.000Z",
      "listId": "string",
      "name": "Ava Chen",
      "order": 1,
      "viewToken": "string",
      "viewType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibility` | string |  |
| `autoCollapseEnabled` | boolean |  |
| `creationTime` | date |  |
| `description` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `isFieldsEditable` | boolean |  |
| `lastModificationTime` | date |  |
| `listId` | string |  |
| `name` | string |  |
| `order` | number |  |
| `viewToken` | string |  |
| `viewType` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `PUT /api/services/app/Views/Update` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-view.md) for the provider-specific parameters and requirements.

