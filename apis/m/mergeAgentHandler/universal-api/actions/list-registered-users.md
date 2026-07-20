# Merge Agent Handler: List Registered Users

Retrieves registered users from Merge Agent Handler.

```
GET https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-registered-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge Agent Handler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-registered-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/list-registered-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge Agent Handler API returns.

## Native endpoint

Through the native Merge Agent Handler API, this operation is `GET /registered-users/` (base URL `https://ah-api.merge.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registered-users.md) for the provider-specific parameters and requirements.

