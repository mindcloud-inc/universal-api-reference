# 1001fx: Format Date and Time

Formats a date and time into a specified output format.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/format-date-and-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/format-date-and-time?connectionId=$CONNECTION_ID&date=string&format=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "format": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/format-date-and-time?${params}`, {
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
| `date` | string | yes | Date value to format. |
| `format` | string | yes | Target date format. |
| `formatsToTest[]` | array | no | Candidate input formats to test before formatting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native 1001fx API, this operation is `POST /datetime/formatdatetime` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/format-date-and-time.md) for the provider-specific parameters and requirements.

