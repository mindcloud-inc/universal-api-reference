# Encodian - Utilities: Utilities - Calculate Date



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-calculate-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-calculate-date?connectionId=$CONNECTION_ID&date=string&measurement=Days&operation=Add&interval=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "measurement": "Days",
  "operation": "Add",
  "interval": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-calculate-date?${params}`, {
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
| `date` | string | yes | The date value to calculate |
| `measurement` | string | yes | Set the time measurement used for the calculation One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. Default: `Days`. |
| `operation` | string | yes | Set the operation type, either add or subtract One of: `0`, `1`. Default: `Add`. |
| `interval` | number | yes | Set amount of time to add or subtract from the 'Date' value provided Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `daysToExclude` | string | no | Specify the days to be excluded from the calculation as a comma-delimited list, for example: Saturday, Sunday |
| `datesToExclude` | string | no | Specify the dates to be excluded from the calculation as a comma-delimited list, for example: 25/12/2024,26/12/2024 |
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
      "result": "string"
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
| `result` | string | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/CalculateDate` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-calculate-date.md) for the provider-specific parameters and requirements.

