# Meisterplan: Create Project

Creates a new project in Meisterplan.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `name` | string | yes | Project name. |
| `start` | string | no | Project start date in YYYY-MM-DD format. |
| `finish` | string | no | Project finish date in YYYY-MM-DD format. |
| `projectKey` | string | no | Unique Meisterplan project key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | no | Project notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "finish": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "program": {
        "id": "string"
      },
      "projectKey": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string | External ID |
| `finish` | date | Project finish date |
| `id` | string | Project ID |
| `name` | string | Project name |
| `notes` | string | Project notes |
| `program.id` | string | Program ID |
| `projectKey` | string | Project key |
| `start` | date | Project start date |
| `viewUrl` | string | View URL |

## Native endpoint

Through the native Meisterplan API, this operation is `POST /scenarios/:scenarioId/projects` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

