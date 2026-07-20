# Calculate Working Day: Is Today A Working Day

Retrieves whether a date is a working day.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/is-today-a-working-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/is-today-a-working-day?connectionId=$CONNECTION_ID&date=2026-05-07T12%3A00%3A00.000Z&working_days=1%2C2%2C3%2C4%2C5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-05-07T12:00:00.000Z",
  "working_days": "1,2,3,4,5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/is-today-a-working-day?${params}`, {
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
| `date` | date | yes | Input date in YYYY-MM-DD format. |
| `working_days` | string | yes | Comma-separated list of working day numbers where Monday is 1. Default: `1,2,3,4,5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input_date": "string",
      "is_input_date_a_working_day": true,
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
| `input_date` | string | Input date returned by the API. |
| `is_input_date_a_working_day` | boolean | Whether the input date is a working day. |
| `message_from_developer` | string | Provider message. |
| `more_info` | string | Provider information URL. |
| `non_working_days` | array<string> | Non-working dates used in the calculation. |
| `working_days` | array<string> | Working day numbers used in the calculation. |
| `working_days_in_words` | array<string> | Working day names used in the calculation. |

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /isTodayAWorkingDay/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/is-today-a-working-day.md) for the provider-specific parameters and requirements.

