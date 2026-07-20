# IdentityCheck: Get Public Verification



```
GET https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-verification?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-verification?${params}`, {
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
| `id` | string | yes | Public verification identifier from a created verification link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "redirectUrl": "https://example.com",
      "response_id": "string",
      "response_type": "string",
      "result": "string",
      "session_token": "string",
      "session_url": "https://example.com",
      "tranche2_flow": {
        "blocked_reason": "string",
        "current_step": "string",
        "enabled": true
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `redirectUrl` | string |  |
| `response_id` | string |  |
| `response_type` | string |  |
| `result` | string |  |
| `session_token` | string |  |
| `session_url` | string |  |
| `tranche2_flow.blocked_reason` | string |  |
| `tranche2_flow.current_step` | string |  |
| `tranche2_flow.enabled` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `GET /public/verification/{id}` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-verification.md) for the provider-specific parameters and requirements.

