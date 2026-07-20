# OnceOnly: List Policies

Retrieves policies from OnceOnly.

```
GET https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/list-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/list-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/list-policies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `GET /v1/policies` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-policies.md) for the provider-specific parameters and requirements.

