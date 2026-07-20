# Aspire: Create As Needed Work Tickets



```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "RouteId": "string",
  "ScheduledStartDate": "string",
  "OpportunityServiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-work-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "RouteId": "string",
    "ScheduledStartDate": "string",
    "OpportunityServiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `EndDateTime` | string | no |  |
| `RouteId` | list<string> | yes |  |
| `ScheduledStartDate` | string | yes |  |
| `StartDateTime` | string | no |  |
| `OpportunityServiceId` | list | yes |  |
| `HoursPerDay` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST WorkTickets/CreateAsNeededWorkTickets` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-work-ticket.md) for the provider-specific parameters and requirements.

