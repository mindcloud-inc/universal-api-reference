# Clockodo: List Entries

Retrieves time entries from your Clockodo account.

```
GET https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockodo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-entries?connectionId=$CONNECTION_ID&limit=25&offset=0&timeSince=string&timeUntil=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "timeSince": "string",
  "timeUntil": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-entries?${params}`, {
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
| `billable` | number | no |  |
| `budgetType` | string | no |  |
| `calcAlsoRevenuesForProjectsWithHardBudget` | boolean | no |  |
| `customersId` | string | no |  |
| `enhancedList` | boolean | no |  |
| `lumpsumServicesId` | string | no |  |
| `projectsId` | string | no |  |
| `servicesId` | string | no |  |
| `text` | string | no |  |
| `textsId` | string | no |  |
| `timeSince` | string | yes | Start of the time range in ISO 8601 UTC. |
| `usersId` | string | no |  |
| `timeUntil` | string | yes | End of the time range in ISO 8601 UTC. |

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

Through the native Clockodo API, this operation is `GET /entries` (base URL `https://my.clockodo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

