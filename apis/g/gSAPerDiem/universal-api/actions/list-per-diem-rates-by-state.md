# GSA Per Diem: List Per Diem Rates by State

Retrieves per diem rates from GSA Per Diem by state.

```
GET https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-per-diem-rates-by-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Per Diem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-per-diem-rates-by-state?connectionId=$CONNECTION_ID&state=VA&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "VA",
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-per-diem-rates-by-state?${params}`, {
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
| `state` | string | yes | Two-letter destination state abbreviation. Example: `VA`. |
| `year` | string | yes | Fiscal year of travel. GSA documents up to three years available. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {},
      "rates": [
        {}
      ],
      "request": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | object | Error details returned by the API; observed as null in successful responses. |
| `rates` | array<object> | Per diem rate results for the requested state and fiscal year. |
| `request` | object | Request metadata returned by the API; observed as null in successful responses. |
| `version` | string | API version field; observed as null in successful responses. |

## Native endpoint

Through the native GSA Per Diem API, this operation is `GET /rates/state/:state/year/:year` (base URL `https://api.gsa.gov/travel/perdiem/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-per-diem-rates-by-state.md) for the provider-specific parameters and requirements.

