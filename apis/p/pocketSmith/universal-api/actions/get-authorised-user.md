# PocketSmith: Get Authorised User

Retrieves the authorised PocketSmith user.

```
GET https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PocketSmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PocketSmith API returns.

## Native endpoint

Through the native PocketSmith API, this operation is `GET /me` (base URL `https://api.pocketsmith.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorised-user.md) for the provider-specific parameters and requirements.

