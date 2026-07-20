# ValidEmail: Verify Email

Verifies an email address with ValidEmail.

```
GET https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ValidEmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | The email address to verify. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AcceptAll": true,
      "Disposable": true,
      "Domain": "string",
      "Email": "ava@example.com",
      "EmailAdditionalInfo": [
        {}
      ],
      "Free": true,
      "IsValid": true,
      "MXRecord": "string",
      "Reason": "string",
      "Role": true,
      "Score": 1,
      "State": "string",
      "Tag": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AcceptAll` | boolean | True when the domain accepts all emails. |
| `Disposable` | boolean | True when the email is disposable or temporary. |
| `Domain` | string | Domain portion of the queried email address. |
| `Email` | string | The queried email address. |
| `EmailAdditionalInfo` | array<object> | Additional provider metadata for the email, reserved for future enhancements. |
| `Free` | boolean | True when the domain is a free email provider. |
| `IsValid` | boolean | True when the email is syntactically and technically valid. |
| `MXRecord` | string | MX record reported for the domain. |
| `Reason` | string | Reason returned by ValidEmail for the verification result. |
| `Role` | boolean | True when the email is role-based. |
| `Score` | number | Confidence score from 0 to 100. |
| `State` | string | Deliverable or Not Deliverable. |
| `Tag` | boolean | True when the email contains a plus-tag. |

## Native endpoint

Through the native ValidEmail API, this operation is `GET /` (base URL `https://api.ValidEmail.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

