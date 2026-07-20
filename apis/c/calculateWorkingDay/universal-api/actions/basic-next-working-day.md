# Calculate Working Day: Basic Next Working Day

Retrieves the next Monday-to-Friday working day.

```
GET https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculate Working Day `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day?connectionId=$CONNECTION_ID&date=2026-04-29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "input_date": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "next_working_day": "string"
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

## Native endpoint

Through the native Calculate Working Day API, this operation is `GET /basicNextWorkingDay/` (base URL `https://api.mightora.io/calculate-working-day`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/basic-next-working-day.md) for the provider-specific parameters and requirements.

