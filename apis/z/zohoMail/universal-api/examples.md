# Zoho Mail Universal API Examples

These examples use the MindCloud API key and Zoho Mail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves all mail accounts from Zoho Mail.

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

Example response:

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

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoMail/latest/actions/list-accounts).

## Apply Labels To Emails

Applies labels to emails in Zoho Mail.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/apply-labels-to-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "labelId[]": "31321431, 222667888"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/apply-labels-to-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "labelId[]": "31321431, 222667888"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "description": "string"
    }
  ],
  "meta": {}
}
```

See the full [Apply Labels To Emails action reference](actions/apply-labels-to-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoMail/latest/actions/apply-labels-to-emails).
