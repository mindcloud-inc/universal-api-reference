# EndBounce: Verify Email

Creates an email verification result in EndBounce.

```
POST https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EndBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "durationMs": 1,
      "email": "ava@example.com",
      "isCatchAll": true,
      "isDisposable": true,
      "isRole": true,
      "mode": "string",
      "reason": "string",
      "score": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `durationMs` | number | Verification duration in milliseconds. |
| `email` | string | Verified email address. |
| `isCatchAll` | boolean | Whether the domain is catch-all. |
| `isDisposable` | boolean | Whether the email is disposable. |
| `isRole` | boolean | Whether the email is a role address. |
| `mode` | string | Response mode for the verification request. |
| `reason` | string | Verification reason code. |
| `score` | number | Verification confidence score. |
| `status` | string | Verification status. |

## Native endpoint

Through the native EndBounce API, this operation is `POST /v1/verify` (base URL `https://api.endbounce.com/api/integrations`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

