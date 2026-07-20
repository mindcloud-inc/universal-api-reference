# Halo Service Solutions: Get Current Agent

Retrieves the current agent from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Halo Service Solutions API returns.

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Agent/me` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-agent.md) for the provider-specific parameters and requirements.

