# Labs64 NetLicensing: Transfer Licenses



```
PUT https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/transfer-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Labs64 NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/transfer-licenses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/transfer-licenses', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Labs64 NetLicensing API returns.

## Native endpoint

Through the native Labs64 NetLicensing API, this operation is `POST /licensee/{licenseeNumber}/transfer` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-licenses.md) for the provider-specific parameters and requirements.

