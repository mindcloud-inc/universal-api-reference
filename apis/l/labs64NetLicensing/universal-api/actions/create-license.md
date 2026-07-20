# Labs64 NetLicensing: Create License



```
POST https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/create-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Labs64 NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/create-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/create-license', {
  method: 'POST',
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

Through the native Labs64 NetLicensing API, this operation is `POST /license` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-license.md) for the provider-specific parameters and requirements.

