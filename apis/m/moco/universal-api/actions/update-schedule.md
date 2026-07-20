# Moco: Update Schedule



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-schedule', {
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
| `absenceCode` | string | no |  |
| `am` | string | no |  |
| `comment` | string | no |  |
| `date` | string | no |  |
| `id` | number | yes |  |
| `overwrite` | string | no |  |
| `pm` | string | no |  |
| `symbol` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "am": true,
      "assignment": {
        "code": "string",
        "color": "string",
        "customerName": "Ava Chen",
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "comment": "string",
      "createdAt": "string",
      "date": "string",
      "id": 1,
      "pm": true,
      "symbol": {},
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
| `am` | boolean |  |
| `assignment` | object |  |
| `assignment.code` | string |  |
| `assignment.color` | string |  |
| `assignment.customerName` | string |  |
| `assignment.id` | number |  |
| `assignment.name` | string |  |
| `assignment.type` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `date` | string |  |
| `id` | number |  |
| `pm` | boolean |  |
| `symbol` | object |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /schedules/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schedule.md) for the provider-specific parameters and requirements.

