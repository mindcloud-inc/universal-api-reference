# ComIDP: Get Asset Details

Retrieves processed asset details from ComIDP.

```
GET https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComIDP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ComIDP API returns.

## Native endpoint

Through the native ComIDP API, this operation is `GET /server/v2/asset/info` (base URL `https://api-server.compdf.com/server/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-details.md) for the provider-specific parameters and requirements.

