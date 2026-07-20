# IdentityCheck: Get Verification



```
GET https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification?${params}`, {
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
| `id` | string | yes | IdentityCheck verification identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "response_id": "string",
      "response_type": "string",
      "result": "string",
      "session_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | string |  |
| `response_id` | string |  |
| `response_type` | string |  |
| `result` | string |  |
| `session_id` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `GET /verification/{id}` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification.md) for the provider-specific parameters and requirements.

