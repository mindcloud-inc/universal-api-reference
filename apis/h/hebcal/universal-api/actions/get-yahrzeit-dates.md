# Hebcal: Get Yahrzeit Dates

Retrieves yahrzeit dates from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-yahrzeit-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-yahrzeit-dates?connectionId=$CONNECTION_ID&y1=string&m1=string&d1=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "y1": "string",
  "m1": "string",
  "d1": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-yahrzeit-dates?${params}`, {
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
| `n1` | string | no | Optional name for the person. |
| `y1` | string | yes | Gregorian year of death. |
| `m1` | string | yes | Gregorian month of death. |
| `d1` | string | yes | Gregorian day of death. |
| `s1` | string | no | Set on if the event occurred after sunset. |
| `years` | string | no | How many Hebrew years to calculate. |
| `start` | string | no | Starting Hebrew year for calculations. |
| `end` | string | no | Ending Hebrew year for calculations. |
| `hebdate` | string | no | Append Hebrew date to event titles. |

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
      "range": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "title": "string",
      "version": "string"
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
| `items[].anniversary` | number |  |
| `items[].category` | string |  |
| `items[].date` | date |  |
| `items[].hdate` | string |  |
| `items[].memo` | string |  |
| `items[].name` | string |  |
| `items[].title` | string |  |
| `range.end` | date |  |
| `range.start` | date |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `POST /yahrzeit` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-yahrzeit-dates.md) for the provider-specific parameters and requirements.

