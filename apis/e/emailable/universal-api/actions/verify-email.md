# Emailable: Verify Email

Verifies an email address in Emailable.

```
GET https://connect.mindcloud.co/v1/universal/emailable/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=john.smith%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "john.smith@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailable/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | The email address you want Emailable to verify. Example: `john.smith@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `smtp` | boolean | no | Set to false to skip the SMTP step and get a faster, less accurate response. |
| `acceptAll` | boolean | no | Set to true to perform an accept-all mailbox check. |
| `timeout` | number | no | How many seconds to wait before Emailable returns a 249 retry-later response. Minimum 2, maximum 10. Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": true,
      "didYouMean": "string",
      "disposable": true,
      "domain": "string",
      "duration": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "free": true,
      "fullName": "Ava Chen",
      "gender": "string",
      "lastName": "Chen",
      "mailboxFull": true,
      "mxRecord": "string",
      "noReply": true,
      "reason": "string",
      "role": true,
      "score": 1,
      "smtpProvider": "string",
      "state": "string",
      "tag": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | boolean | Whether the domain appears to accept all recipient addresses. |
| `didYouMean` | string | A suggested corrected email address when Emailable detects a likely typo. |
| `disposable` | boolean | Whether the address belongs to a disposable email provider. |
| `domain` | string | The domain portion of the verified email address. |
| `duration` | number | How long the verification took, in seconds. |
| `email` | string | The email address that was verified. |
| `firstName` | string | The inferred first name associated with the email address. |
| `free` | boolean | Whether the address belongs to a free email provider. |
| `fullName` | string | The inferred full name associated with the email address. |
| `gender` | string | The inferred gender associated with the email address. |
| `lastName` | string | The inferred last name associated with the email address. |
| `mailboxFull` | boolean | Whether the mailbox appears to be full. |
| `mxRecord` | string | The MX record Emailable resolved for the domain. |
| `noReply` | boolean | Whether the address appears to be a no-reply mailbox. |
| `reason` | string | The primary reason Emailable assigned the verification outcome. |
| `role` | boolean | Whether the address appears to be a role-based inbox. |
| `score` | number | Emailable's quality score for the email address. |
| `smtpProvider` | string | The SMTP provider Emailable detected for the address. |
| `state` | string | The overall verification state returned by Emailable. |
| `tag` | string | The optional Emailable tag value associated with the verification. |
| `user` | string | The local-part user portion of the email address. |

## Native endpoint

Through the native Emailable API, this operation is `GET /v1/verify` (base URL `https://api.emailable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

