# Syncro: Create Ticket Timer

Creates a ticket timer entry in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-ticket-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-ticket-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-ticket-timer', {
  method: 'POST',
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
| `id` | number | yes | The Syncro ticket ID. |
| `startAt` | date | no |  |
| `endAt` | date | no |  |
| `durationMinutes` | number | no |  |
| `userId` | number | no |  |
| `notes` | string | no |  |
| `productId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeDuration": 1,
      "billable": true,
      "billableOverride": 1,
      "billableTime": 1,
      "commentId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "productId": 1,
      "recorded": true,
      "startTime": "2026-05-07T12:00:00.000Z",
      "ticketId": 1,
      "ticketLineItemId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeDuration` | number |  |
| `billable` | boolean |  |
| `billableOverride` | number |  |
| `billableTime` | number |  |
| `commentId` | number |  |
| `createdAt` | date |  |
| `endTime` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `productId` | number |  |
| `recorded` | boolean |  |
| `startTime` | date |  |
| `ticketId` | number |  |
| `ticketLineItemId` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /tickets/:id/timer_entry` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-timer.md) for the provider-specific parameters and requirements.

