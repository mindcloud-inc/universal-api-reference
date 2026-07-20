# Clockodo: Start Clock

Starts the clock in your Clockodo account.

```
POST https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/start-clock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/start-clock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customersId": "string",
  "servicesId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/start-clock', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customersId": "string",
    "servicesId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | number | no |  |
| `customersId` | string | yes | Customer ID for the running clock entry. |
| `projectsId` | string | no |  |
| `text` | string | no |  |
| `usersId` | string | no |  |
| `servicesId` | string | yes | Service ID for the running clock entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": 1,
      "budgetType": "string",
      "calcAlsoRevenuesForProjectsWithHardBudget": true,
      "customersId": "string",
      "duration": 1,
      "enhancedList": true,
      "hourlyRate": 1,
      "id": "string",
      "lumpsum": 1,
      "lumpsumServicesAmount": 1,
      "lumpsumServicesId": "string",
      "projectsId": "string",
      "servicesId": "string",
      "text": "string",
      "textsId": "string",
      "timeSince": "string",
      "timeUntil": "string",
      "usersId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | number |  |
| `budgetType` | string |  |
| `calcAlsoRevenuesForProjectsWithHardBudget` | boolean |  |
| `customersId` | string |  |
| `duration` | number |  |
| `enhancedList` | boolean |  |
| `hourlyRate` | number |  |
| `id` | string |  |
| `lumpsum` | number |  |
| `lumpsumServicesAmount` | number |  |
| `lumpsumServicesId` | string |  |
| `projectsId` | string |  |
| `servicesId` | string |  |
| `text` | string |  |
| `textsId` | string |  |
| `timeSince` | string |  |
| `timeUntil` | string |  |
| `usersId` | string |  |

## Native endpoint

Through the native Clockodo API, this operation is `POST /clock` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-clock.md) for the provider-specific parameters and requirements.

