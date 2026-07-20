# MailboxValidator: Check Disposable Email



```
GET https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-disposable-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailboxValidator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-disposable-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-disposable-email?${params}`, {
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
| `email` | string | yes | Email address to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsAvailable": 1,
      "emailAddress": "ava@example.com",
      "isDisposable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsAvailable` | number |  |
| `emailAddress` | string |  |
| `isDisposable` | boolean |  |

## Native endpoint

Through the native MailboxValidator API, this operation is `GET /v2/email/disposable` (base URL `https://api.mailboxvalidator.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-disposable-email.md) for the provider-specific parameters and requirements.

