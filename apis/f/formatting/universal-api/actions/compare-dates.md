# Formatting: Compare Dates

Compares two dates in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/compare-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/compare-dates?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/compare-dates?${params}`, {
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
| `startDate` | string | yes | The first date to compare. |
| `endDate` | string | yes | The second date to compare. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "days": 1,
      "hours": 1,
      "milliseconds": 1,
      "minutes": 1,
      "same": true,
      "seconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days` | number |  |
| `hours` | number |  |
| `milliseconds` | number |  |
| `minutes` | number |  |
| `same` | boolean |  |
| `seconds` | number |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-dates.md) for the provider-specific parameters and requirements.

