# GSA Per Diem: List CONUS M&IE Breakdown Rates

Retrieves CONUS M&IE breakdown rates from GSA Per Diem.

```
GET https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Per Diem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates?connectionId=$CONNECTION_ID&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-mie-breakdown-rates?${params}`, {
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
| `year` | string | yes | Fiscal year of travel. GSA documents up to three years available. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakfast": 1,
      "dinner": 1,
      "FirstLastDay": 1,
      "incidental": 1,
      "lunch": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakfast` | number | Daily breakfast meal rate. |
| `dinner` | number | Daily dinner meal rate. |
| `FirstLastDay` | number | First and last travel day total. |
| `incidental` | number | Daily incidental expense rate. |
| `lunch` | number | Daily lunch meal rate. |
| `total` | number | Total meals and incidental expense per diem. |

## Native endpoint

Through the native GSA Per Diem API, this operation is `GET /rates/conus/mie/:year` (base URL `https://api.gsa.gov/travel/perdiem/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conus-mie-breakdown-rates.md) for the provider-specific parameters and requirements.

