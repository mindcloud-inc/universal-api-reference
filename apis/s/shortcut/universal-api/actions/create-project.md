# Shortcut: Create Project



```
POST https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "teamId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `teamId` | number | yes |  |
| `description` | string | no |  |
| `color` | string | no |  |
| `iterationLength` | number | no |  |
| `abbreviation` | string | no |  |
| `externalId` | string | no |  |
| `startTime` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "entityType": "string",
      "id": 1,
      "name": "Ava Chen",
      "startTime": "2026-05-07T12:00:00.000Z",
      "teamId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string |  |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `entityType` | string |  |
| `id` | number |  |
| `name` | string |  |
| `startTime` | date |  |
| `teamId` | number |  |
| `updatedAt` | date |  |
| `workflowId` | number |  |

## Native endpoint

Through the native Shortcut API, this operation is `POST /projects` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

