# IPLocate: Batch Lookup



```
GET https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/batch-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPLocate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/batch-lookup?connectionId=$CONNECTION_ID&ips%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ips[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/batch-lookup?${params}`, {
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
| `ips[]` | array<string> | yes | Array of IPv4 or IPv6 addresses to look up in one request. IPLocate allows between 1 and 1000 items per batch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPLocate API returns.

## Native endpoint

Through the native IPLocate API, this operation is `POST /batch` (base URL `https://iplocate.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-lookup.md) for the provider-specific parameters and requirements.

