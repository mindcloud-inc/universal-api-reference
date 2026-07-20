# MyEmailVerifier: Verify Email

Retrieves an email verification result from MyEmailVerifier by address.

```
GET https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/verify-email?${params}`, {
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
      "Address": "string",
      "catch_all": 1,
      "Diagnosis": "string",
      "Disposable_Domain": 1,
      "Free_Domain": 1,
      "Greylisted": 1,
      "Role_Based": 1,
      "Status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string | Email address that was verified. |
| `catch_all` | number | Whether the domain accepts all recipients as 0 or 1. |
| `Diagnosis` | string | Provider diagnosis for the verification result. |
| `Disposable_Domain` | number | Whether the address uses a disposable domain as 0 or 1. |
| `Free_Domain` | number | Whether the address uses a free email provider as 0 or 1. |
| `Greylisted` | number | Whether the destination is greylisted as 0 or 1. |
| `Role_Based` | number | Whether the address is a role-based inbox as 0 or 1. |
| `Status` | string | Verification result status. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `GET /verifier/validate_single/:email/{{credentials.apiKey}}` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

