# Avaza: Create Task

Creates a new task in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectidfk": 1,
  "sectionidfk": 1,
  "title": "string",
  "assignedtouseridfks": 1,
  "tags": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectidfk": 1,
    "sectionidfk": 1,
    "title": "string",
    "assignedtouseridfks": 1,
    "tags": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectidfk` | number | yes |  |
| `sectionidfk` | number | yes |  |
| `accounttasktypeidfk` | number | no |  |
| `title` | string | yes |  |
| `description` | string | no |  |
| `assignedtouseridfks` | list<number> | yes |  |
| `taskprioritycode` | string | no |  |
| `datestart` | date | no |  |
| `datedue` | date | no |  |
| `estimatedeffort` | number | no | Decimal hours |
| `tags` | list<object> | yes | Collection of tags specifying Name and Color (Hex) |
| `tags[].name` | string | no |  |
| `tags[].color` | string | no | Hex color code in format #000000 |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Task` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

