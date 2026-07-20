# remberg: Get Asset By Number

Retrieves an asset from remberg by asset number.

```
GET https://connect.mindcloud.co/v1/universal/remberg/latest/actions/get-asset-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a remberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/get-asset-by-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remberg/latest/actions/get-asset-by-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native remberg API returns.

## Native endpoint

Through the native remberg API, this operation is `GET /v2/assets/number/{assetNumber}` (base URL `https://api.remberg.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-by-number.md) for the provider-specific parameters and requirements.

