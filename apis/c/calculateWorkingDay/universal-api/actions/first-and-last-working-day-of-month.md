# Calculate Working Day: First And Last Working Day Of Month

Retrieves a month's first and last working days.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/first-and-last-working-day-of-month
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/first-and-last-working-day-of-month?connectionId=$CONNECTION_ID&date=2026-04-29&working_days=1%2C2%2C3%2C4%2C5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-29",
  "working_days": "1,2,3,4,5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/first-and-last-working-day-of-month?${params}`, {
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
| `date` | date | yes | Input date in YYYY-MM-DD format. Example: `2026-04-29`. |
| `working_days` | string | yes | Comma-separated weekday numbers where Monday is 1. Default is 1,2,3,4,5. Default: `1,2,3,4,5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "first_working_day_of_month": "string",
      "input_date": "string",
      "last_working_day_of_month": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "non_working_days": [
        "string"
      ],
      "working_days": [
        "string"
      ],
      "working_days_in_words": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `first_working_day_of_month` | string | First working day in the input date's month. |
| `input_date` | string | Input date returned by the API. |
| `last_working_day_of_month` | string | Last working day in the input date's month. |
| `message_from_developer` | string | Provider message. |
| `more_info` | string | Provider information URL. |
| `non_working_days` | array<string> | Non-working dates used in the calculation. |
| `working_days` | array<string> | Working day numbers used in the calculation. |
| `working_days_in_words` | array<string> | Working day names used in the calculation. |

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /firstAndLastWorkingDayOfMonth/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/first-and-last-working-day-of-month.md) for the provider-specific parameters and requirements.

