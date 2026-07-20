# Clockify: Generate Shared Report

Generates a shared report in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-shared-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-shared-report?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/generate-shared-report?${params}`, {
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
| `dateRangeEnd` | string | no |  |
| `dateRangeStart` | string | no |  |
| `exportType` | string | no |  |
| `id` | string | yes |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `sortColumn` | string | no |  |
| `sortOrder` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chart": [
        [
          {}
        ]
      ],
      "groupOne": [
        [
          {}
        ]
      ],
      "totals": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chart[]` | array<object> |  |
| `chart[].earned` | number |  |
| `chart[].id` | string |  |
| `chart[].totalAmount` | number |  |
| `chart[].totalBillableTime` | number |  |
| `chart[].totalTime` | number |  |
| `groupOne[]` | array<object> |  |
| `groupOne[].amount` | number |  |
| `groupOne[].children[]` | array<object> |  |
| `groupOne[].children[].amount` | number |  |
| `groupOne[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].children[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].children[].clientName` | string |  |
| `groupOne[].children[].children[].days[]` | array<object> |  |
| `groupOne[].children[].children[].days[].amount` | number |  |
| `groupOne[].children[].children[].days[].date` | string |  |
| `groupOne[].children[].children[].days[].duration` | number |  |
| `groupOne[].children[].children[].duration` | number |  |
| `groupOne[].children[].children[].id` | string |  |
| `groupOne[].children[].children[].name` | string |  |
| `groupOne[].children[].children[].nameLowerCase` | string |  |
| `groupOne[].children[].clientName` | string |  |
| `groupOne[].children[].days[]` | array<object> |  |
| `groupOne[].children[].days[].amount` | number |  |
| `groupOne[].children[].days[].date` | string |  |
| `groupOne[].children[].days[].duration` | number |  |
| `groupOne[].children[].duration` | number |  |
| `groupOne[].children[].id` | string |  |
| `groupOne[].children[].name` | string |  |
| `groupOne[].children[].nameLowerCase` | string |  |
| `groupOne[].clientName` | string |  |
| `groupOne[].days[]` | array<object> |  |
| `groupOne[].days[].amount` | number |  |
| `groupOne[].days[].date` | string |  |
| `groupOne[].days[].duration` | number |  |
| `groupOne[].duration` | number |  |
| `groupOne[].id` | string |  |
| `groupOne[].name` | string |  |
| `groupOne[].nameLowerCase` | string |  |
| `totals[]` | array<object> |  |
| `totals[].amounts[]` | array<object> |  |
| `totals[].amounts[].type` | string |  |
| `totals[].amounts[].value` | number |  |
| `totals[].entriesCount` | number |  |
| `totals[].id` | string |  |
| `totals[].totalBillableTime` | number |  |
| `totals[].totalTime` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET shared-reports/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-shared-report.md) for the provider-specific parameters and requirements.

