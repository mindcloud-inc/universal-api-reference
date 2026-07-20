# Kickbox: Verify Email

Verifies an email address with Kickbox.

```
GET https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kickbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | The email address to verify, URL-encoded. |
| `timeout` | number | no | Maximum time in milliseconds for the verification request. Default 6000, maximum 30000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_all": true,
      "did_you_mean": "string",
      "disposable": true,
      "domain": "string",
      "email": "ava@example.com",
      "free": true,
      "message": "string",
      "reason": "string",
      "result": "string",
      "role": true,
      "sendex": 1,
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
| `accept_all` | boolean | Whether the domain appears configured as accept-all. |
| `did_you_mean` | string | Suggested correction for a likely typo in the email address. |
| `disposable` | boolean | Whether the address appears disposable or temporary. |
| `domain` | string | Domain portion of the email address. |
| `email` | string | Normalized email address returned by Kickbox. |
| `free` | boolean | Whether the address belongs to a free email provider. |
| `message` | string | Provider message returned with the verification result. |
| `reason` | string | Specific reason associated with the verification outcome. |
| `result` | string | Top-level verification outcome for the email address. |
| `role` | boolean | Whether the address appears to be a role account. |
| `sendex` | number | Kickbox Sendex quality score for the email address. |
| `success` | boolean | Whether the verification request succeeded. |
| `user` | string | Local-part user portion of the email address. |

## Native endpoint

Through the native Kickbox API, this operation is `GET /verify` (base URL `https://api.kickbox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

