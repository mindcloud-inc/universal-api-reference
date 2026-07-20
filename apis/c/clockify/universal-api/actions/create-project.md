# Clockify: Create Project

Creates a new project in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `costRate.amount` | number | no |  |
| `costRate.since` | date | no |  |
| `estimate.estimate` | string | no |  |
| `estimate.type` | list<string> | no | One of: `AUTO`, `MANUAL`. |
| `hourlyRate.amount` | number | no |  |
| `hourlyRate.since` | date | no |  |
| `workspaceId` | list<string> | yes |  |
| `name` | string | yes |  |
| `billable` | boolean | no |  |
| `clientId` | string | no |  |
| `color` | string | no |  |
| `costRate` | object | no |  |
| `estimate` | object | no |  |
| `hourlyRate` | object | no |  |
| `isPublic` | boolean | no |  |
| `note` | string | no |  |
| `memberships[]` | array<object> | no |  |
| `tasks[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "clientId": "string",
      "clientName": "Ava Chen",
      "color": "string",
      "costRate": {},
      "duration": "string",
      "estimate": {},
      "hourlyRate": {},
      "id": "string",
      "memberships": [
        {}
      ],
      "name": "Ava Chen",
      "note": "string",
      "public": true,
      "template": true,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billable` | boolean |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `color` | string |  |
| `costRate` | object |  |
| `duration` | string |  |
| `estimate` | object |  |
| `hourlyRate` | object |  |
| `id` | string |  |
| `memberships` | array<object> |  |
| `name` | string |  |
| `note` | string |  |
| `public` | boolean |  |
| `template` | boolean |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/projects` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

