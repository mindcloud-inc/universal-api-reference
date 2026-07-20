# ConfigCat: Get Authenticated User Details

Retrieves authenticated user details from ConfigCat.

```
GET https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConfigCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConfigCat API returns.

## Native endpoint

Through the native ConfigCat API, this operation is `GET /v1/me` (base URL `https://api.configcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user-details.md) for the provider-specific parameters and requirements.

