# Paymo: Update Time Entry

Updates an existing time entry in Paymo.

```
PUT https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryId` | number | yes | The Paymo time entry id. |
| `duration` | number | no | Updated duration in seconds for date-based entries. |
| `description` | string | no | Updated time entry description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedManually": true,
      "billed": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "date": "string",
      "description": "string",
      "duration": 1,
      "id": 1,
      "isBulk": true,
      "price": 1,
      "projectId": 1,
      "status": "string",
      "taskId": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedManually` | boolean |  |
| `billed` | boolean |  |
| `createdOn` | date |  |
| `date` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `isBulk` | boolean |  |
| `price` | number |  |
| `projectId` | number |  |
| `status` | string |  |
| `taskId` | number |  |
| `updatedOn` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Paymo API, this operation is `PUT entries/:entryId` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

