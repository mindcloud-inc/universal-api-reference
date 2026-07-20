# Clockodo: Get Currently Running Entries

Retrieves currently running entries from your Clockodo account.

```
GET https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/get-currently-running-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/get-currently-running-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/get-currently-running-entries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Clockodo API, this operation is `GET /clock` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currently-running-entries.md) for the provider-specific parameters and requirements.

