# Didit: Remove from Blocklist

Removes an entry from the Didit blocklist.

```
DELETE https://connect.mindcloud.co/v1/universal/didit/latest/actions/remove-from-blocklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/didit/latest/actions/remove-from-blocklist?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/remove-from-blocklist?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Didit API returns.

## Native endpoint

Through the native Didit API, this operation is `POST /blocklist/remove/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-from-blocklist.md) for the provider-specific parameters and requirements.

