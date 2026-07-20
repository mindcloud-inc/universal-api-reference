# Asset Infinity: Get User Groups

Retrieves user groups from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-user-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-user-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asset Infinity API returns.

## Native endpoint

Through the native Asset Infinity API, this operation is `POST GetUserGroupAPI` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-groups.md) for the provider-specific parameters and requirements.

