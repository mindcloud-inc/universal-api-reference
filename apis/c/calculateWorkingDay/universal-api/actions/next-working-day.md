# Calculate Working Day: Next Working Day

Retrieves the next working day using custom working-day rules.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/next-working-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/next-working-day?connectionId=$CONNECTION_ID&date=2026-04-29&working_days=1%2C2%2C3%2C4%2C5&x_working_days=4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-29",
  "working_days": "1,2,3,4,5",
  "x_working_days": "4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/next-working-day?${params}`, {
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
| `x_working_days` | number | yes | Number of working days to look ahead. Default: `4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `non_working_days` | string | no | Optional comma-separated dates to exclude in YYYY-MM-DD format. Example: `2026-12-25,2026-12-26`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input_date": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "next_working_day": "string",
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
| `message_from_developer` | string | Provider message. |
| `more_info` | string | Provider information URL. |
| `next_working_day` | string | Next working day after the input date. |
| `non_working_days` | array<string> | Non-working dates used in the calculation. |
| `working_days` | array<string> | Working day numbers used in the calculation. |
| `working_days_in_words` | array<string> | Working day names used in the calculation. |

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /nextWorkingDay/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/next-working-day.md) for the provider-specific parameters and requirements.

