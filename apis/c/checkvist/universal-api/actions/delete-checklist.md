# Checkvist: Delete Checklist

Deletes a checklist from Checkvist.

```
DELETE https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-checklist?connectionId=$CONNECTION_ID&checklistId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklistId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/delete-checklist?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The checklist ID. |

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

Through the native Checkvist API, this operation is `DELETE /checklists/:checklistId.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-checklist.md) for the provider-specific parameters and requirements.

