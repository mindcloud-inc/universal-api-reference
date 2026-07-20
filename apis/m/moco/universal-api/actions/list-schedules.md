# Moco: List Schedules



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-schedules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `absenceCode` | string | no |  |
| `customProperties` | object | no |  |
| `from` | date | no |  |
| `holidayRequestId` | number | no |  |
| `ids` | string | no |  |
| `to` | date | no |  |
| `updatedAfter` | date | no |  |
| `userId` | number | no |  |

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

Through the native Moco API, this operation is `GET /schedules` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedules.md) for the provider-specific parameters and requirements.

