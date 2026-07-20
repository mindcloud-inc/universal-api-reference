# Checkvist: Create Checklist

Creates a checklist in Checkvist.

```
POST https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-checklist', {
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
| `name` | string | yes | The checklist name. |
| `public` | boolean | no | Set to 1 to create a public checklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": 1,
      "itemCount": 1,
      "name": "Ava Chen",
      "options": 1,
      "percentCompleted": 1,
      "public": true,
      "readOnly": true,
      "relatedTaskIds": [
        1
      ],
      "tags": {},
      "tagsAsText": "string",
      "taskCompleted": 1,
      "taskCount": 1,
      "updatedAt": "string",
      "userCount": 1,
      "userUpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `id` | number |  |
| `itemCount` | number |  |
| `name` | string |  |
| `options` | number |  |
| `percentCompleted` | number |  |
| `public` | boolean |  |
| `readOnly` | boolean |  |
| `relatedTaskIds` | array<number> |  |
| `tags` | object |  |
| `tagsAsText` | string |  |
| `taskCompleted` | number |  |
| `taskCount` | number |  |
| `updatedAt` | string |  |
| `userCount` | number |  |
| `userUpdatedAt` | string |  |

## Native endpoint

Through the native Checkvist API, this operation is `POST /checklists.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist.md) for the provider-specific parameters and requirements.

