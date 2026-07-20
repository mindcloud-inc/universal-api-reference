# Meisterplan: Create Milestone

Creates a new milestone in Meisterplan.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "projectId": "string",
  "name": "Ava Chen",
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-milestone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "projectId": "string",
    "name": "Ava Chen",
    "date": "string"
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
| `name` | string | yes | Milestone name. |
| `date` | string | yes | Milestone date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "projectPhase": {
        "name": "Ava Chen"
      },
      "status": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Milestone date |
| `id` | string | Milestone ID |
| `name` | string | Milestone name |
| `projectPhase.name` | string | Project phase name |
| `status.value` | string | Milestone status |

## Native endpoint

Through the native Meisterplan API, this operation is `POST /scenarios/:scenarioId/projects/:projectId/milestones` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-milestone.md) for the provider-specific parameters and requirements.

