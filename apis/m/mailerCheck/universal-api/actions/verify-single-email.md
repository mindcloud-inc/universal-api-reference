# MailerCheck: Verify Single Email

Retrieves a real-time email verification result from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/verify-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/verify-single-email?${params}`, {
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
| `email` | string | yes | Email address to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native MailerCheck API, this operation is `POST /check/single` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-single-email.md) for the provider-specific parameters and requirements.

