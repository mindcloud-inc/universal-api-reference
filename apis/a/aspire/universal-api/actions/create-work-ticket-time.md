# Aspire: Create Work Ticket Time

Creates a new work ticket time in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "startTime": "2026-05-07T12:00:00.000Z",
  "endTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket-time', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "startTime": "2026-05-07T12:00:00.000Z",
    "endTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no |  |
| `workTicketId` | number | no |  |
| `startTime` | date | yes |  |
| `startLatitude` | number | no |  |
| `startLongitude` | number | no |  |
| `routeId` | number | no |  |
| `crewLeaderContactId` | number | no |  |
| `endTime` | date | yes |  |
| `endLatitude` | number | no |  |
| `endLongitude` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `POST WorkTicketTimes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-work-ticket-time.md) for the provider-specific parameters and requirements.

