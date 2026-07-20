# GSA Per Diem: List CONUS Lodging Rates

Retrieves CONUS lodging rates from GSA Per Diem.

```
GET https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-lodging-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Per Diem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-lodging-rates?connectionId=$CONNECTION_ID&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-lodging-rates?${params}`, {
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
      "Apr": "string",
      "Aug": "string",
      "City": "string",
      "County": "string",
      "Dec": "string",
      "DID": "string",
      "Feb": "string",
      "Jan": "string",
      "Jul": "string",
      "Jun": "string",
      "Mar": "string",
      "May": "string",
      "Meals": "string",
      "Nov": "string",
      "Oct": "string",
      "Sep": "string",
      "State": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Apr` | string | April lodging rate per day. |
| `Aug` | string | August lodging rate per day. |
| `City` | string | Destination city or Standard Rate. |
| `County` | string | Destination county or counties. |
| `Dec` | string | December lodging rate per day. |
| `DID` | string | Destination ID for the city/state pair. |
| `Feb` | string | February lodging rate per day. |
| `Jan` | string | January lodging rate per day. |
| `Jul` | string | July lodging rate per day. |
| `Jun` | string | June lodging rate per day. |
| `Mar` | string | March lodging rate per day. |
| `May` | string | May lodging rate per day. |
| `Meals` | string | Meal rate per day. |
| `Nov` | string | November lodging rate per day. |
| `Oct` | string | October lodging rate per day. |
| `Sep` | string | September lodging rate per day. |
| `State` | string | Destination state. |

## Native endpoint

Through the native GSA Per Diem API, this operation is `GET /rates/conus/lodging/:year` (base URL `https://api.gsa.gov/travel/perdiem/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conus-lodging-rates.md) for the provider-specific parameters and requirements.

