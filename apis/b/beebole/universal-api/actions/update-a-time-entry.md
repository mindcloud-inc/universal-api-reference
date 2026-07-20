# Beebole: Update a Time Entry

Updates an existing time entry in Beebole.

```
PUT https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "date": "2026-03-23",
  "hours": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "date": "2026-03-23",
    "hours": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Beebole time entry identifier. |
| `company.id` | number | no | Optional company identifier when moving a time entry to a company-level target. Example: `25`. |
| `project.id` | number | no | Optional project identifier when moving a time entry to a project-level target. Example: `26`. |
| `subproject.id` | number | no | Optional subproject identifier when moving a time entry to a subproject-level target. Example: `37`. |
| `task.id` | number | no | Optional task identifier. Required when tasks exist for the selected entity and the entry is not an absence. Example: `19`. |
| `date` | string | yes | The time entry date in YYYY-MM-DD format. Example: `2026-03-23`. |
| `hours` | number | yes | The number of hours to store on the time entry. Example: `2`. |
| `comment` | string | no | Optional comment stored on the time entry. Example: `Updated from MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `absence.id` | number | no | Optional absence identifier when converting a time entry to an absence entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-time-entry.md) for the provider-specific parameters and requirements.

