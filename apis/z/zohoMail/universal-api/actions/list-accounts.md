# Zoho Mail: List Accounts

Retrieves all mail accounts from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCreationTime": 1,
      "accountDisplayName": "Ava Chen",
      "accountId": "string",
      "accountName": "Ava Chen",
      "activeSyncEnabled": true,
      "address": {},
      "allowedStorage": 1,
      "country": "string",
      "deliveryType": "string",
      "displayName": "Ava Chen",
      "emailAddress": [
        {}
      ],
      "enabled": true,
      "extraEdiscoveryStorage": {},
      "extraStorage": {},
      "firstName": "Ava",
      "gender": "string",
      "iamStatus": 1,
      "iamUserRole": "string",
      "imapAccessEnabled": true,
      "imapBlocked": true,
      "incomingBlocked": true,
      "incomingUserName": "Ava Chen",
      "isDefaultAccount": true,
      "isDesignatedMailbox": true,
      "isLogoExist": true,
      "language": "string",
      "lastClient": "string",
      "lastLogin": 1,
      "lastName": "Chen",
      "mailboxAddress": "string",
      "mailboxCreationTime": 1,
      "mailboxStatus": "string",
      "mxStatus": true,
      "outgoingBlocked": true,
      "planStorage": 1,
      "planType": 1,
      "policyId": {},
      "popAccessEnabled": true,
      "popBlocked": true,
      "popFetchTime": 1,
      "primaryEmailAddress": "ava@example.com",
      "role": "string",
      "sendMailDetails": [
        {}
      ],
      "sequence": 1,
      "smtpStatus": true,
      "spamcheckEnabled": true,
      "status": true,
      "tfaEnabled": true,
      "timeZone": "string",
      "type": "string",
      "uri": "string",
      "usedStorage": 1,
      "userExpiry": 1,
      "webBlocked": true,
      "zuid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCreationTime` | number | Account creation timestamp |
| `accountDisplayName` | string | Account display name |
| `accountId` | string | Account identifier |
| `accountName` | string | Account name |
| `activeSyncEnabled` | boolean | ActiveSync enabled flag |
| `address` | object | Address details |
| `allowedStorage` | number | Allowed storage amount |
| `country` | string | Account country code |
| `deliveryType` | string | Delivery type |
| `displayName` | string | Display name |
| `emailAddress` | array<object> | Email addresses for the account |
| `enabled` | boolean | Enabled flag |
| `extraEdiscoveryStorage` | object | Extra e-discovery storage details |
| `extraStorage` | object | Extra storage details |
| `firstName` | string | First name |
| `gender` | string | Gender value |
| `iamStatus` | number | IAM status code |
| `iamUserRole` | string | IAM user role |
| `imapAccessEnabled` | boolean | IMAP access enabled flag |
| `imapBlocked` | boolean | IMAP blocked flag |
| `incomingBlocked` | boolean | Incoming mail blocked flag |
| `incomingUserName` | string | Incoming username |
| `isDefaultAccount` | boolean | Default account flag |
| `isDesignatedMailbox` | boolean | Designated mailbox flag |
| `isLogoExist` | boolean | Logo availability flag |
| `language` | string | Account language |
| `lastClient` | string | Last client name |
| `lastLogin` | number | Last login timestamp |
| `lastName` | string | Last name |
| `mailboxAddress` | string | Mailbox address |
| `mailboxCreationTime` | number | Mailbox creation timestamp |
| `mailboxStatus` | string | Mailbox status |
| `mxStatus` | boolean | MX status enabled flag |
| `outgoingBlocked` | boolean | Outgoing blocked flag |
| `planStorage` | number | Plan storage allocation |
| `planType` | number | Plan type code |
| `policyId` | object | Policy identifiers |
| `popAccessEnabled` | boolean | POP access enabled flag |
| `popBlocked` | boolean | POP access blocked flag |
| `popFetchTime` | number | POP fetch timestamp |
| `primaryEmailAddress` | string | Primary email address |
| `role` | string | Account role |
| `sendMailDetails` | array<object> | Send mail details |
| `sequence` | number | Account sequence |
| `smtpStatus` | boolean | SMTP status flag |
| `spamcheckEnabled` | boolean | Spam check enabled flag |
| `status` | boolean | Account status flag |
| `tfaEnabled` | boolean | Two-factor enabled flag |
| `timeZone` | string | Account time zone |
| `type` | string | Account type |
| `uri` | string | Account API URI |
| `usedStorage` | number | Used storage amount |
| `userExpiry` | number | User expiry timestamp |
| `webBlocked` | boolean | Web access blocked flag |
| `zuid` | number | Zoho user identifier |

## Native endpoint

Through the native Zoho Mail API, this operation is `GET /accounts` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

