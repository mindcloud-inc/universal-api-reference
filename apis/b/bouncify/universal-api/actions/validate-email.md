# Bouncify: Validate Email

Validates an email address with Bouncify.

```
GET https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | Email address to validate with Bouncify. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `disposable` | number | Disposable-email indicator as returned by Bouncify. |
| `domain` | string | Domain extracted from the email address. |
| `email` | string | The email address that was checked. |
| `freeEmail` | number | Free-email-provider indicator as returned by Bouncify. |
| `message` | string | Provider message describing the result. |
| `result` | string | Verification result returned by Bouncify. |
| `role` | number | Role-account indicator as returned by Bouncify. |
| `spamtrap` | number | Spamtrap indicator as returned by Bouncify. |
| `success` | boolean | Whether the verification request succeeded. |
| `user` | string | Local-part extracted from the email address. |

## Native endpoint

Through the native Bouncify API, this operation is `GET /verify` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

