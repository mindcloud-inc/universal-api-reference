# Halo Service Solutions: Create Project

Creates a new project in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `summary` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "datecreated": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "guid": "string",
      "id": 1,
      "is_project": true,
      "reference": "string",
      "site_id": 1,
      "site_name": "Ava Chen",
      "status_id": 1,
      "summary": "string",
      "team": "string",
      "team_id": 1,
      "tickettype_id": 1,
      "user_id": 1,
      "user_name": "Ava Chen",
      "workflow_id": 1,
      "workflow_step": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `datecreated` | date |  |
| `details` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `is_project` | boolean |  |
| `reference` | string |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `status_id` | number |  |
| `summary` | string |  |
| `team` | string |  |
| `team_id` | number |  |
| `tickettype_id` | number |  |
| `user_id` | number |  |
| `user_name` | string |  |
| `workflow_id` | number |  |
| `workflow_step` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Projects` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

