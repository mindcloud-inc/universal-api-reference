# Instantly: Create Account

Creates a new account in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "providerCode": 1,
  "imapUsername": "Ava Chen",
  "imapPassword": "string",
  "imapHost": "string",
  "imapPort": 1,
  "smtpUsername": "Ava Chen",
  "smtpPassword": "string",
  "smtpHost": "string",
  "smtpPort": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "providerCode": 1,
    "imapUsername": "Ava Chen",
    "imapPassword": "string",
    "imapHost": "string",
    "imapPort": 1,
    "smtpUsername": "Ava Chen",
    "smtpPassword": "string",
    "smtpHost": "string",
    "smtpPort": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the account. |
| `firstName` | string | yes | First name associated with the account. |
| `lastName` | string | yes | Last name associated with the account. |
| `providerCode` | number | yes | Provider code for the account: 1 Custom IMAP/SMTP, 2 Google, 3 Microsoft, 4 AWS, 8 AirMail. |
| `imapUsername` | string | yes | IMAP username. |
| `imapHost` | string | yes | IMAP host. |
| `imapPort` | number | yes | IMAP port. |
| `smtpUsername` | string | yes | SMTP username. |
| `smtpHost` | string | yes | SMTP host. |
| `smtpPort` | number | yes | SMTP port. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imapPassword` | string | yes | IMAP password. |
| `smtpPassword` | string | yes | SMTP password. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "provider_code": 1,
      "status": 1,
      "timestamp_created": "2026-05-07T12:00:00.000Z",
      "timestamp_updated": "2026-05-07T12:00:00.000Z",
      "warmup_status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address of the account. |
| `first_name` | string | First name associated with the account. |
| `last_name` | string | Last name associated with the account. |
| `provider_code` | number | Provider code for the account. |
| `status` | number | Current status of the account. |
| `timestamp_created` | date | Timestamp when the account was created. |
| `timestamp_updated` | date | Timestamp when the account was last updated. |
| `warmup_status` | number | Current warmup status. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/accounts` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

