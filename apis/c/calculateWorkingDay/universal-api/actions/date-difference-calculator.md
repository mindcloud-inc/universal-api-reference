# Calculate Working Day: Date Difference Calculator

Retrieves total and working-day counts between two dates.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/date-difference-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/date-difference-calculator?connectionId=$CONNECTION_ID&start_date=2026-05-07T12%3A00%3A00.000Z&end_date=2026-05-07T12%3A00%3A00.000Z&working_days=1%2C2%2C3%2C4%2C5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start_date": "2026-05-07T12:00:00.000Z",
  "end_date": "2026-05-07T12:00:00.000Z",
  "working_days": "1,2,3,4,5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/date-difference-calculator?${params}`, {
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
| `start_date` | date | yes | Start date in YYYY-MM-DD format. |
| `end_date` | date | yes | End date in YYYY-MM-DD format. |
| `working_days` | string | yes | Comma-separated list of working day numbers where Monday is 1. Default: `1,2,3,4,5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `non_working_days` | string | no | Optional comma-separated dates in YYYY-MM-DD format to treat as non-working days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_date": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "non_working_days": [
        "string"
      ],
      "start_date": "string",
      "total_days": 1,
      "working_days": [
        "string"
      ],
      "working_days_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_date` | string | End date returned by the API. |
| `message_from_developer` | string | Provider message. |
| `more_info` | string | Provider information URL. |
| `non_working_days` | array<string> | Non-working days included in the calculation. |
| `start_date` | string | Start date returned by the API. |
| `total_days` | number | Total days between the start and end dates. |
| `working_days` | array<string> | Working days included in the calculation. |
| `working_days_count` | number | Count of working days between the start and end dates. |

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /dateDifferenceCalculator/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/date-difference-calculator.md) for the provider-specific parameters and requirements.

