# Noor: List Space Members

Retrieves members for a Noor space.

```
GET https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Noor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noor/latest/actions/list-space-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Noor API returns.

## Native endpoint

Through the native Noor API, this operation is `POST /getSpaceMembers` (base URL `https://sun.noor.to/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-members.md) for the provider-specific parameters and requirements.

