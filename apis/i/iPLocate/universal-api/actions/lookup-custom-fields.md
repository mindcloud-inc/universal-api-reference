# IPLocate: Lookup Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPLocate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-custom-fields?connectionId=$CONNECTION_ID&ip=string&include=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string",
  "include": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-custom-fields?${params}`, {
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
| `ip` | string | yes | IPv4 or IPv6 address to look up. |
| `include` | string | yes | Comma-separated list of fields or nested fields to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPLocate API returns.

## Native endpoint

Through the native IPLocate API, this operation is `GET /lookup/:ip` (base URL `https://iplocate.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-custom-fields.md) for the provider-specific parameters and requirements.

