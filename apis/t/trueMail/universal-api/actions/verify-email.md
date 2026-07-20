# TrueMail: Verify Email

Validates an email address in TrueMail.

```
GET https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/verify-email?${params}`, {
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
| `validationType` | string | no | Choose MX for standard validation or SMTP for premium mailbox checks. One of: `0`, `1`. Default: `mx`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "email": "ava@example.com",
      "result": {},
      "status": "string",
      "validationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `email` | string |  |
| `result` | object |  |
| `status` | string |  |
| `validationType` | string |  |

## Native endpoint

Through the native TrueMail API, this operation is `POST /v1/verify` (base URL `https://api.mailcop.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

