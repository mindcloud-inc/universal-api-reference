# Formatting: Add/Subtract Time

Adds or subtracts time in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/add-subtract-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/add-subtract-time?connectionId=$CONNECTION_ID&input=string&operationMode=string&duration=1&unit=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "operationMode": "string",
  "duration": "1",
  "unit": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/add-subtract-time?${params}`, {
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
| `input` | string | yes | The starting date or time value. |
| `operationMode` | string | yes | Whether to add or subtract time. |
| `duration` | number | yes | The amount of time to add or subtract. |
| `unit` | string | yes | The time unit to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateTime` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subtract-time.md) for the provider-specific parameters and requirements.

