# Moco: Create Activity



```
POST https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | string | no |  |
| `date` | string | no |  |
| `description` | string | no |  |
| `projectId` | string | no |  |
| `remoteId` | string | no |  |
| `remoteService` | string | no |  |
| `remoteUrl` | string | no |  |
| `seconds` | string | no |  |
| `tag` | string | no |  |
| `taskId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billed": true,
      "createdAt": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "date": "string",
      "description": "string",
      "hourlyRate": 1,
      "hours": 1,
      "id": 1,
      "invoiceId": {},
      "project": {
        "billable": true,
        "id": 1,
        "name": "Ava Chen"
      },
      "remoteId": {},
      "remoteService": "string",
      "remoteUrl": {},
      "seconds": 1,
      "tag": "string",
      "task": {
        "billable": true,
        "id": 1,
        "name": "Ava Chen"
      },
      "timerStartedAt": {},
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "workedSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billed` | boolean |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `date` | string |  |
| `description` | string |  |
| `hourlyRate` | number |  |
| `hours` | number |  |
| `id` | number |  |
| `invoiceId` | object |  |
| `project` | object |  |
| `project.billable` | boolean |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `remoteId` | object |  |
| `remoteService` | string |  |
| `remoteUrl` | object |  |
| `seconds` | number |  |
| `tag` | string |  |
| `task` | object |  |
| `task.billable` | boolean |  |
| `task.id` | number |  |
| `task.name` | string |  |
| `timerStartedAt` | object |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `workedSeconds` | number |  |

## Native endpoint

Through the native Moco API, this operation is `POST /activities` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

