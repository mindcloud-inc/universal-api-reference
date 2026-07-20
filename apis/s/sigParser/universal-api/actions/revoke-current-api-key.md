# SigParser: Revoke Current API Key



```
DELETE https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/revoke-current-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/revoke-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/revoke-current-api-key?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigParser API returns.

## Native endpoint

Through the native SigParser API, this operation is `DELETE /api/User/Invalidate` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-current-api-key.md) for the provider-specific parameters and requirements.

