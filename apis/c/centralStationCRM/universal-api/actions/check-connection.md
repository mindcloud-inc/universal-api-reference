# CentralStationCRM: Check Connection

Checks the current CentralStationCRM API connection.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/check-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/check-connection?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CentralStationCRM API returns.

## Native endpoint

Through the native CentralStationCRM API, this operation is `GET /api/check_connection` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-connection.md) for the provider-specific parameters and requirements.

