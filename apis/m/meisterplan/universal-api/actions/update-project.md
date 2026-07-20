# Meisterplan: Update Project

Updates an existing project in Meisterplan.

```
PUT https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `projectId` | string | yes | Internal Meisterplan project identifier. |
| `name` | string | no | Updated project name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | no | Updated project notes. |

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

Through the native Meisterplan API, this operation is `PATCH /scenarios/:scenarioId/projects/:projectId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

