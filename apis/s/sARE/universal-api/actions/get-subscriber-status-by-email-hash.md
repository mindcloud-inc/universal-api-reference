# SARE: Get Subscriber Status By Email Hash

Retrieves subscriber status from SARE by email hash.

```
GET https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-status-by-email-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-status-by-email-hash?connectionId=$CONNECTION_ID&emailHash=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailHash": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sARE/latest/actions/get-subscriber-status-by-email-hash?${params}`, {
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
| `emailHash` | string | yes | MD5 hash for the subscriber email, derived from the SARE account salt and email value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SARE API returns.

## Native endpoint

Through the native SARE API, this operation is `GET /email/status_hash/:emailHash` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-status-by-email-hash.md) for the provider-specific parameters and requirements.

