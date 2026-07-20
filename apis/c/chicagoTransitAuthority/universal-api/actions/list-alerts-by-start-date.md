# Chicago Transit Authority: List Alerts by Start Date

Finds alerts in Chicago Transit Authority by start date.

```
GET https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-alerts-by-start-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chicago Transit Authority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-alerts-by-start-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-alerts-by-start-date?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chicago Transit Authority API returns.

## Native endpoint

Through the native Chicago Transit Authority API, this operation is `GET /alerts.aspx` (base URL `https://lapi.transitchicago.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts-by-start-date.md) for the provider-specific parameters and requirements.

