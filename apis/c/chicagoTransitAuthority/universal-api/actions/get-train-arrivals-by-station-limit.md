# Chicago Transit Authority: Get Train Arrivals by Station Limit

Retrieves limited train arrival predictions in Chicago Transit Authority by station.

```
GET https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chicago Transit Authority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station-limit?connectionId=$CONNECTION_ID&mapId=string&max=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string",
  "max": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station-limit?${params}`, {
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
| `mapId` | string | yes | CTA station map ID, such as 40380 for Clark/Lake. |
| `max` | number | yes | Maximum number of arrivals to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chicago Transit Authority API returns.

## Native endpoint

Through the native Chicago Transit Authority API, this operation is `GET /ttarrivals.aspx` (base URL `https://lapi.transitchicago.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-train-arrivals-by-station-limit.md) for the provider-specific parameters and requirements.

