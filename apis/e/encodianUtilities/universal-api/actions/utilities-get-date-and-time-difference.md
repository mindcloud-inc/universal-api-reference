# Encodian - Utilities: Utilities - Get Date and Time Difference



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-get-date-and-time-difference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-get-date-and-time-difference?connectionId=$CONNECTION_ID&startDateTime=string&endDateTime=string&interval=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTime": "string",
  "endDateTime": "string",
  "interval": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-get-date-and-time-difference?${params}`, {
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
| `startDateTime` | string | yes | Start date (and optionally time) of the period to be calculated |
| `endDateTime` | string | yes | End date (and optionally time) of the period to be calculated |
| `interval` | string | yes | The interval to calculate - Year, Quarter, Month, Week, Day, Hour, Minute, Second, Millisecond One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `daysToExclude` | string | no | Specify the days to be excluded from the calculation as a comma-delimited list, for example: Saturday, Sunday |
| `cultureName` | string | no | Change the thread culture used to process the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `result` | number | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/GetDateTimeDifference` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-get-date-and-time-difference.md) for the provider-specific parameters and requirements.

