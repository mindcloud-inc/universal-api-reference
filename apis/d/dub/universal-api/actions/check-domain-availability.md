# Dub: Check Domain Availability

Checks domain availability in Dub.

```
GET https://connect.mindcloud.co/v1/universal/dub/latest/actions/check-domain-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dub/latest/actions/check-domain-availability?connectionId=$CONNECTION_ID&domains%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domains[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dub/latest/actions/check-domain-availability?${params}`, {
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
| `domains[]` | array<string> | yes | One or more .link domains to check. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dub API returns.

## Native endpoint

Through the native Dub API, this operation is `GET /domains/status` (base URL `https://api.dub.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-availability.md) for the provider-specific parameters and requirements.

