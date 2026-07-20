# Beebole: Create a Time Entry

Creates a new time entry in Beebole.

```
POST https://connect.mindcloud.co/v1/universal/beebole/latest/actions/create-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/create-a-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-03-23",
  "hours": "1.5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/create-a-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-03-23",
    "hours": "1.5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company.id` | number | no | Optional company identifier when creating a company-level time entry. Example: `25`. |
| `project.id` | number | no | Optional project identifier when creating a project-level time entry. Example: `26`. |
| `subproject.id` | number | no | Optional subproject identifier when creating a subproject-level time entry. Example: `37`. |
| `task.id` | number | no | Optional task identifier. Required when tasks exist for the selected entity and the entry is not an absence. Example: `19`. |
| `date` | string | yes | The work date for the time entry in YYYY-MM-DD format. Example: `2026-03-23`. |
| `hours` | number | yes | The number of hours to log. Example: `1.5`. |
| `comment` | string | no | Optional comment stored on the time entry. Example: `Draft entry from MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `absence.id` | number | no | Optional absence identifier when creating an absence time entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-time-entry.md) for the provider-specific parameters and requirements.

