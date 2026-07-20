# Instant: Verify Magic Code

Verifies a magic code in Instant.

```
POST https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-magic-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-magic-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-magic-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | User email address tied to the magic code. |
| `code` | string | yes | Magic code to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": true,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | boolean | Whether verifying the code created a new user. |
| `user` | object | Instant user verified from the magic code. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/verify_magic_code` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-magic-code.md) for the provider-specific parameters and requirements.

