# Aspire: Create Clock Time



```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-clock-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-clock-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactID": "string",
  "clockStartDateTime": "2026-05-07T12:00:00.000Z",
  "clockEndDateTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-clock-time', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactID": "string",
    "clockStartDateTime": "2026-05-07T12:00:00.000Z",
    "clockEndDateTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactID` | list | yes |  |
| `clockStartDateTime` | date | yes |  |
| `clockEndDateTime` | date | yes |  |
| `RouteID` | list | no | Either Route ID or Crew Leader Contact ID field is required |
| `crewLeaderContactID` | list | no | Either Route ID or Crew Leader Contact ID field is required |
| `BreakTime` | number | no |  |
| `ClockStartLat` | number | no |  |
| `ClockStartLong` | number | no |  |
| `ClockEndLat` | number | no |  |
| `ClockEndLong` | number | no |  |

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

Through the native Aspire API, this operation is `POST ClockTimes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-clock-time.md) for the provider-specific parameters and requirements.

