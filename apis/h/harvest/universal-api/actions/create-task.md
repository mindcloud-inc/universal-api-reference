# Harvest: Create Task

Creates a new task in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-task', {
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
| `billableByDefault` | boolean | no |  |
| `defaultHourlyRate` | number | no |  |
| `isDefault` | boolean | no |  |
| `isActive` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billableByDefault": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultHourlyRate": 1,
      "id": 1,
      "isActive": true,
      "isDefault": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableByDefault` | boolean |  |
| `createdAt` | date |  |
| `defaultHourlyRate` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `POST /v2/tasks` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

