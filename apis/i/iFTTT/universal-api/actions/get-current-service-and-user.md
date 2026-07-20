# IFTTT: Get Current Service and User



```
GET https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IFTTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IFTTT API returns.

## Native endpoint

Through the native IFTTT API, this operation is `GET /v2/me` (base URL `https://connect.ifttt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-service-and-user.md) for the provider-specific parameters and requirements.

