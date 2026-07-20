# Checkvist: Update Checklist

Updates a checklist in Checkvist.

```
PUT https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklistId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/update-checklist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklistId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The checklist ID. |
| `name` | string | no | The checklist name. |
| `public` | boolean | no | Set to 1 to make the checklist public. |

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

Through the native Checkvist API, this operation is `PUT /checklists/:checklistId.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-checklist.md) for the provider-specific parameters and requirements.

