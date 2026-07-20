# Hebcal: Get Torah Readings for Date Range

Retrieves Torah readings for a date range from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-torah-readings-for-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-torah-readings-for-date-range?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-torah-readings-for-date-range?${params}`, {
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
| `start` | string | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | string | yes | Gregorian end date in YYYY-MM-DD format. |
| `i` | string | no | Use Israel Torah reading schedule when enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "items": [
        [
          {}
        ]
      ],
      "location": "string",
      "range": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `items[]` | array<object> |  |
| `items[].date` | date |  |
| `items[].hdate` | string |  |
| `items[].name.en` | string |  |
| `items[].name.he` | string |  |
| `items[].parshaNum[]` | array<number> |  |
| `items[].summary` | string |  |
| `items[].type` | string |  |
| `items[].weekday.1.b` | string |  |
| `items[].weekday.1.e` | string |  |
| `items[].weekday.1.k` | string |  |
| `items[].weekday.1.v` | number |  |
| `items[].weekday.2.b` | string |  |
| `items[].weekday.2.e` | string |  |
| `items[].weekday.2.k` | string |  |
| `items[].weekday.2.v` | number |  |
| `items[].weekday.3.b` | string |  |
| `items[].weekday.3.e` | string |  |
| `items[].weekday.3.k` | string |  |
| `items[].weekday.3.v` | number |  |
| `location` | string |  |
| `range.end` | date |  |
| `range.start` | date |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /leyning` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-torah-readings-for-date-range.md) for the provider-specific parameters and requirements.

