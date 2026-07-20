# Cloudmersive: Parse Natural Language Date and Time

Parses a natural language date and time in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-natural-language-date-and-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-natural-language-date-and-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-natural-language-date-and-time?${params}`, {
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
| `RawDateTimeInput` | string | no | Natural language date-time string to parse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "day": 1,
      "dayOfWeek": "string",
      "hour": 1,
      "minute": 1,
      "month": 1,
      "parsedDateResult": "2026-05-07T12:00:00.000Z",
      "second": 1,
      "successful": true,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `day` | number |  |
| `dayOfWeek` | string |  |
| `hour` | number |  |
| `minute` | number |  |
| `month` | number |  |
| `parsedDateResult` | date |  |
| `second` | number |  |
| `successful` | boolean |  |
| `year` | number |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/date-time/parse/date-time/natural-language` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-natural-language-date-and-time.md) for the provider-specific parameters and requirements.

