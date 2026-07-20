# BuildBetter: List Signals by Date Range



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-signals-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-signals-by-date-range?connectionId=$CONNECTION_ID&dateFrom=2026-01-01T00%3A00%3A00&dateTo=2026-01-31T23%3A59%3A59" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "2026-01-01T00:00:00",
  "dateTo": "2026-01-31T23:59:59"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-signals-by-date-range?${params}`, {
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
| `dateFrom` | string | yes | Start of the display timestamp window. Example: `2026-01-01T00:00:00`. |
| `dateTo` | string | yes | End of the display timestamp window. Example: `2026-01-31T23:59:59`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of signals to return. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call": {},
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "interview_id": "string",
      "person_id": "string",
      "sentiment": 1,
      "speaker": 1,
      "summary": "string",
      "types": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call` | object | Linked call summary. |
| `display_ts` | date | Signal display timestamp. |
| `id` | string | BuildBetter signal identifier. |
| `interview_id` | string | Linked call identifier. |
| `person_id` | string | Linked person identifier. |
| `sentiment` | number | Signal sentiment score. |
| `speaker` | number | Speaker code for the signal. |
| `summary` | string | Signal summary text. |
| `types` | array<object> | Signal type assignments. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signals-by-date-range.md) for the provider-specific parameters and requirements.

