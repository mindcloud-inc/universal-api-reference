# RotaCloud: Update Logbook Entry



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-logbook-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-logbook-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "description": "string",
  "categoryId": 1,
  "date": "string",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-logbook-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen",
    "description": "string",
    "categoryId": 1,
    "date": "string",
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Logbook entry ID. |
| `name` | string | yes | Logbook entry name. |
| `description` | string | yes | Logbook entry description. |
| `categoryId` | number | yes | Logbook category ID. |
| `date` | string | yes | Entry date in YYYY-MM-DD format. |
| `userId` | number | yes | User ID for the logbook entry. |
| `time` | string | no | Entry time in HH:mm format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "createdAt": "string",
      "createdBy": 1,
      "date": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "time": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `createdAt` | string |  |
| `createdBy` | number |  |
| `date` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `time` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `PUT /v2/logbook/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-logbook-entry.md) for the provider-specific parameters and requirements.

