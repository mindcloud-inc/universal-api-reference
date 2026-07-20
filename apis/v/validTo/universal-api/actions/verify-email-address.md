# validTo: Verify Email Address

Verifies an email address with validTo.

```
GET https://connect.mindcloud.co/v1/universal/validTo/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a validTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validTo/latest/actions/verify-email-address?${params}`, {
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
| `email` | string | yes | The email address to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": 1,
      "disposable": 1,
      "domain": "string",
      "email": "ava@example.com",
      "freeEmail": 1,
      "message": "string",
      "result": "string",
      "role": 1,
      "spamtrap": 1,
      "success": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | number | Whether the domain accepts mail for any address. |
| `disposable` | number | Whether the email is disposable. |
| `domain` | string | The domain part of the verified email address. |
| `email` | string | The verified email address. |
| `freeEmail` | number | Whether the email uses a free email provider. |
| `message` | string | Human-readable result description from validTo. |
| `result` | string | Verification outcome for the email address. |
| `role` | number | Whether the email is a role address. |
| `spamtrap` | number | Whether the email is a spam trap. |
| `success` | boolean | Whether the verification request succeeded. |
| `user` | string | The local-part of the verified email address. |

## Native endpoint

Through the native validTo API, this operation is `GET /verify` (base URL `https://api.validto.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.

