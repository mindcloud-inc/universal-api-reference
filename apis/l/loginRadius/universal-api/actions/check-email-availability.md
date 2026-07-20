# LoginRadius: Check Email Availability

Checks whether an email is available in LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/check-email-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/check-email-availability?connectionId=$CONNECTION_ID&email=loginradius-stage3-20260401162148%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "loginradius-stage3-20260401162148@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/check-email-availability?${params}`, {
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
| `email` | string | yes | Email address to verify availability or retrieve the associated account. Example: `loginradius-stage3-20260401162148@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `verificationToken` | string | no | Verification token received in email. Example: `verification-token`. |
| `otp` | string | no | One-time passcode sent to the user's email. Example: `123456`. |
| `preventWebhook` | boolean | no | When true, suppresses webhook events for this operation. |
| `uuid` | string | no | Email template UUID for welcome email flows. Example: `welcome-template-uuid`. |
| `url` | string | no | URL to log the main domain in the database. Example: `https://example.com/welcome`. |
| `welcomeEmailTemplate` | string | no | Welcome email template name. Example: `welcome_template`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isExist": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isExist` | boolean |  |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/email` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-email-availability.md) for the provider-specific parameters and requirements.

