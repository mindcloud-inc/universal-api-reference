# ProProfs Project: Get Time Entry

Retrieves a time entry from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-time-entry?${params}`, {
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
| `entryId` | string | yes | The time entry ID to fetch. |

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

Through the native ProProfs Project API, this operation is `GET /time_entries/{{entry_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

