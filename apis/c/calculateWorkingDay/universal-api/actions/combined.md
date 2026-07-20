# Calculate Working Day: Combination Of All Calculate Working Day Endpoints

Retrieves combined results from all working-day calculations.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/combined
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/combined?connectionId=$CONNECTION_ID&date=2026-05-07T12%3A00%3A00.000Z&working_days=1%2C2%2C3%2C4%2C5&x_working_days=4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-05-07T12:00:00.000Z",
  "working_days": "1,2,3,4,5",
  "x_working_days": "4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/combined?${params}`, {
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
| `x_working_days` | number | yes | Number of working days to add. Default: `4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `non_working_days` | string | no | Optional comma-separated dates in YYYY-MM-DD format to treat as non-working days. |
| `country` | list | no | Optional country value for bank holiday filtering. One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "first_working_day_of_month": "string",
      "input_date": "string",
      "is_input_date_a_working_day": true,
      "last_working_day_of_month": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "next_working_day": "string",
      "non_working_days": [
        "string"
      ],
      "working_day_in_x_days": "string",
      "working_days": [
        "string"
      ],
      "working_days_in_words": [
        "string"
      ],
      "x_days": 1
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
| `is_input_date_a_working_day` | boolean | Whether the input date is a working day. |
| `last_working_day_of_month` | string | Last working day in the input date's month. |
| `message_from_developer` | string | Provider message. |
| `more_info` | string | Provider information URL. |
| `next_working_day` | string | Next working day after the input date. |
| `non_working_days` | array<string> | Non-working dates used in the calculation. |
| `working_day_in_x_days` | string | Working day found after adding the requested number of working days. |
| `working_days` | array<string> | Working day numbers used in the calculation. |
| `working_days_in_words` | array<string> | Working day names used in the calculation. |
| `x_days` | number | Number of working days added to the input date. |

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /combined/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/combined.md) for the provider-specific parameters and requirements.

