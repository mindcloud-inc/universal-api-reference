# Workiom: Create List

Creates a new list in your Workiom workspace.

```
POST https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-list', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "icon": "string",
      "id": "string",
      "isVisible": true,
      "lastModificationTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `creationTime` | date |  |
| `description` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `isVisible` | boolean |  |
| `lastModificationTime` | date |  |
| `name` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `POST /api/services/app/Lists/Create` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

