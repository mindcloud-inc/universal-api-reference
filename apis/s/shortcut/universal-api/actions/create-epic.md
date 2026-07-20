# Shortcut: Create Epic



```
POST https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-epic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-epic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-epic', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | no |  |
| `state` | string | no |  |
| `milestoneId` | number | no |  |
| `requestedById` | string | no |  |
| `epicStateId` | number | no |  |
| `groupId` | string | no |  |
| `externalId` | string | no |  |
| `deadline` | string | no |  |
| `plannedStartDate` | string | no |  |
| `completedAtOverride` | string | no |  |
| `startedAtOverride` | string | no |  |
| `convertedFromStoryId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "entityType": "string",
      "epicStateId": 1,
      "groupId": "string",
      "id": 1,
      "milestoneId": 1,
      "name": "Ava Chen",
      "requestedById": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `entityType` | string |  |
| `epicStateId` | number |  |
| `groupId` | string |  |
| `id` | number |  |
| `milestoneId` | number |  |
| `name` | string |  |
| `requestedById` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Shortcut API, this operation is `POST /epics` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-epic.md) for the provider-specific parameters and requirements.

