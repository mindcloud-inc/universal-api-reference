# ComEd: Get 5-Minute Prices By Time Range

Retrieves 5-minute prices from ComEd for a time range.

```
GET https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get5-minute-prices-by-time-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComEd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get5-minute-prices-by-time-range?connectionId=$CONNECTION_ID&dateStart=202604200000&dateEnd=202604200100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateStart": "202604200000",
  "dateEnd": "202604200100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get5-minute-prices-by-time-range?${params}`, {
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
| `dateStart` | string | yes | Inclusive start timestamp in the documented ComEd format YYYYMMDDhhmm. Example: `202604200000`. |
| `dateEnd` | string | yes | Inclusive end timestamp in the documented ComEd format YYYYMMDDhhmm. Example: `202604200100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "millisUTC": "string",
      "price": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `millisUTC` | string | UTC timestamp in milliseconds as returned by the ComEd public feed. |
| `price` | string | Price in cents per kWh as returned by the ComEd public feed. |

## Native endpoint

Through the native ComEd API, this operation is `GET /api` (base URL `https://hourlypricing.comed.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get5-minute-prices-by-time-range.md) for the provider-specific parameters and requirements.

