# EmailVerify.io: Validate Email

Validates an email address with EmailVerify.io.

```
GET https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailVerify.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | Email address to validate with EmailVerify.io. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "status": "string",
      "subStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The email address that was checked. |
| `status` | string | Overall verification result. |
| `subStatus` | string | Detailed verification sub-status. |

## Native endpoint

Through the native EmailVerify.io API, this operation is `GET /validate` (base URL `https://app.emailverify.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

