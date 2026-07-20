# ProxiedMail: List Received Email Links



```
GET https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-received-email-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-received-email-links?connectionId=$CONNECTION_ID&proxyBindingId=1FA46A03-F100-0000-00000BAE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "proxyBindingId": "1FA46A03-F100-0000-00000BAE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-received-email-links?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `proxyBindingId` | string | yes | Example: `1FA46A03-F100-0000-00000BAE`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProxiedMail API returns.

## Native endpoint

Through the native ProxiedMail API, this operation is `GET /received-emails-links/:proxyBindingId` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-received-email-links.md) for the provider-specific parameters and requirements.

