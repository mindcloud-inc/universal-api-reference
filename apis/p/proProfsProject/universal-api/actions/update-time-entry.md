# ProProfs Project: Update Time Entry

Updates an existing time entry in ProProfs Project.

```
PUT https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entryId": "string",
  "seconds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entryId": "string",
    "seconds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The updated time entry description. |
| `entryId` | string | yes | The time entry ID to update. |
| `seconds` | string | yes | The total seconds for the updated entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billed": 1,
      "date": "string",
      "dateStarted": "string",
      "dateStopped": "string",
      "description": "string",
      "entryId": "string",
      "hours": 1,
      "minutes": 1,
      "projectId": "string",
      "projectName": "Ava Chen",
      "seconds": "string",
      "subtaskId": "string",
      "subtaskName": "Ava Chen",
      "taskId": "string",
      "taskName": "Ava Chen",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billed` | number |  |
| `date` | string |  |
| `dateStarted` | string |  |
| `dateStopped` | string |  |
| `description` | string |  |
| `entryId` | string |  |
| `hours` | number |  |
| `minutes` | number |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `seconds` | string |  |
| `subtaskId` | string |  |
| `subtaskName` | string |  |
| `taskId` | string |  |
| `taskName` | string |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `PUT /time_entries/{{entry_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

