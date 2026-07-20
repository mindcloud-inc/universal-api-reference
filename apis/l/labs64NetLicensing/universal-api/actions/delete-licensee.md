# Labs64 NetLicensing: Delete Licensee



```
DELETE https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/delete-licensee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Labs64 NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/delete-licensee?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/delete-licensee?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Labs64 NetLicensing API returns.

## Native endpoint

Through the native Labs64 NetLicensing API, this operation is `DELETE /licensee/{licenseeNumber}` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-licensee.md) for the provider-specific parameters and requirements.

