# Chicago Transit Authority: List Systemwide Statuses

Retrieves systemwide statuses in Chicago Transit Authority.

```
GET https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-systemwide-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chicago Transit Authority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-systemwide-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/list-systemwide-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chicago Transit Authority API returns.

## Native endpoint

Through the native Chicago Transit Authority API, this operation is `GET /routes.aspx` (base URL `https://lapi.transitchicago.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-systemwide-statuses.md) for the provider-specific parameters and requirements.

