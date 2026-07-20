# International Monetary Fund: Get Indicator Time Series

Retrieves IMF time series for a single indicator.

```
GET https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/get-indicator-time-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a International Monetary Fund `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/get-indicator-time-series?connectionId=$CONNECTION_ID&indicatorId=NGDP_RPCH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indicatorId": "NGDP_RPCH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/get-indicator-time-series?${params}`, {
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
| `indicatorId` | string | yes | IMF indicator identifier, such as NGDP_RPCH for real GDP growth. Example: `NGDP_RPCH`. |
| `periods` | string | no | Optional comma-separated list of years to restrict the series, for example 2019,2020. Example: `2019,2020`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Indicator identifier. |
| `values` | object | Mapping of entity identifiers to period-value maps. |

## Native endpoint

Through the native International Monetary Fund API, this operation is `GET /:indicatorId` (base URL `https://www.imf.org/external/datamapper/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator-time-series.md) for the provider-specific parameters and requirements.

