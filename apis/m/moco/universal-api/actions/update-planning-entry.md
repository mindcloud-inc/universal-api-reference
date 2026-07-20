# Moco: Update Planning Entry



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-planning-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-planning-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-planning-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no |  |
| `dealId` | string | no |  |
| `endsOn` | string | no |  |
| `hoursPerDay` | string | no |  |
| `id` | number | yes |  |
| `projectId` | string | no |  |
| `startsOn` | string | no |  |
| `symbol` | string | no |  |
| `tentative` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "comment": "string",
      "createdAt": "string",
      "deal": {},
      "endsOn": "string",
      "hoursPerDay": 1,
      "id": 1,
      "project": {
        "color": "string",
        "customerName": "Ava Chen",
        "id": 1,
        "identifier": "string",
        "name": "Ava Chen"
      },
      "readOnly": true,
      "seriesId": {},
      "seriesRepeat": {},
      "startsOn": "string",
      "symbol": {},
      "task": {},
      "tentative": true,
      "title": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `deal` | object |  |
| `endsOn` | string |  |
| `hoursPerDay` | number |  |
| `id` | number |  |
| `project` | object |  |
| `project.color` | string |  |
| `project.customerName` | string |  |
| `project.id` | number |  |
| `project.identifier` | string |  |
| `project.name` | string |  |
| `readOnly` | boolean |  |
| `seriesId` | object |  |
| `seriesRepeat` | object |  |
| `startsOn` | string |  |
| `symbol` | object |  |
| `task` | object |  |
| `tentative` | boolean |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /planning_entries/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-planning-entry.md) for the provider-specific parameters and requirements.

