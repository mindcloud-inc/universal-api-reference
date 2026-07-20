# InstantCard: Authenticate User

Retrieves an authentication token from InstantCard by user credentials.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/authenticate-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/authenticate-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/authenticate-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InstantCard API returns.

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/authenticate?email={{credentials.email}}&password={{credentials.password}}` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-user.md) for the provider-specific parameters and requirements.

