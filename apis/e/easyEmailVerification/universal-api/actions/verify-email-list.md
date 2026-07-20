# Easy Email Verification: Verify Email List

Retrieves verification results for up to 50 emails in Easy Email Verification.

```
GET https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/verify-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Email Verification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/verify-email-list?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/verify-email-list?${params}`, {
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
| `emails[]` | array<string> | yes | List of email addresses to verify. Max size is 50. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy Email Verification API returns.

## Native endpoint

Through the native Easy Email Verification API, this operation is `POST /verify` (base URL `https://api.easyemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-list.md) for the provider-specific parameters and requirements.

