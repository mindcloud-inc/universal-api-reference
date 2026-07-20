# MailboxValidator: Validate Email Address



```
GET https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/validate-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailboxValidator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/validate-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/validate-email-address?${params}`, {
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
| `email` | string | yes | Email address to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseEmailAddress": "ava@example.com",
      "creditsAvailable": 1,
      "domain": "string",
      "emailAddress": "ava@example.com",
      "isCatchall": true,
      "isDisposable": true,
      "isDmarcEnforced": true,
      "isDomain": true,
      "isFree": true,
      "isGreylisted": true,
      "isHighRisk": true,
      "isRole": true,
      "isServerDown": true,
      "isSmtp": true,
      "isStrictSpf": true,
      "isSuppressed": true,
      "isSyntax": true,
      "isVerified": true,
      "mailboxvalidatorScore": 1,
      "status": true,
      "timeTaken": 1,
      "websiteExist": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseEmailAddress` | string |  |
| `creditsAvailable` | number |  |
| `domain` | string |  |
| `emailAddress` | string |  |
| `isCatchall` | boolean |  |
| `isDisposable` | boolean |  |
| `isDmarcEnforced` | boolean |  |
| `isDomain` | boolean |  |
| `isFree` | boolean |  |
| `isGreylisted` | boolean |  |
| `isHighRisk` | boolean |  |
| `isRole` | boolean |  |
| `isServerDown` | boolean |  |
| `isSmtp` | boolean |  |
| `isStrictSpf` | boolean |  |
| `isSuppressed` | boolean |  |
| `isSyntax` | boolean |  |
| `isVerified` | boolean |  |
| `mailboxvalidatorScore` | number |  |
| `status` | boolean |  |
| `timeTaken` | number |  |
| `websiteExist` | boolean |  |

## Native endpoint

Through the native MailboxValidator API, this operation is `GET /v2/validation/single` (base URL `https://api.mailboxvalidator.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-address.md) for the provider-specific parameters and requirements.

