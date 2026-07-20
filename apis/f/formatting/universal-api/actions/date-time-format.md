# Formatting: Date/Time Format

Formats a date or time in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/date-time-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/date-time-format?connectionId=$CONNECTION_ID&input=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "outputFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/date-time-format?${params}`, {
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
| `input` | string | yes | The date or time value to format. |
| `outputFormat` | string | yes | The output date format pattern. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedDateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedDateTime` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/date-time-format.md) for the provider-specific parameters and requirements.

