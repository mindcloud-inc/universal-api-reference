# FindyMail: Verify Email

Verifies an email address with FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "john@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Email address to verify for deliverability. Example: `john@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "provider": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address that was verified. |
| `provider` | string | Detected email provider. |
| `verified` | boolean | Whether FindyMail verified the email as deliverable. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/verify` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

