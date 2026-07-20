# ShareFile Universal API Examples

These examples use the MindCloud API key and ShareFile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Session



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session?${params}`, {
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
      "AuthenticationType": "string",
      "Id": "string",
      "IsAuthenticated": true,
      "OAuth2ClientName": "Ava Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "Principal": {},
      "Tool": "string",
      "url": "https://example.com",
      "Version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Session action reference](actions/get-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shareFile/latest/actions/get-session).

## Create Client User



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-client-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Email": "ava@example.com",
  "FirstName": "Ava",
  "LastName": "Chen",
  "Company": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-client-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Email": "ava@example.com",
    "FirstName": "Ava",
    "LastName": "Chen",
    "Company": "string"
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
      "Company": "string",
      "Contacted": 1,
      "DateCreated": "string",
      "Domain": "string",
      "Email": "ava@example.com",
      "EmailAddresses": [
        {}
      ],
      "Emails": [
        "ava@example.com"
      ],
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "FullNameShort": "Ava Chen",
      "Id": "string",
      "Initials": "string",
      "IsBillingContact": true,
      "IsConfirmed": true,
      "IsDeleted": true,
      "LastName": "Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "ReferredBy": "string",
      "Roles": [
        "string"
      ],
      "TotalSharedFiles": 1,
      "url": "https://example.com",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Client User action reference](actions/create-client-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shareFile/latest/actions/create-client-user).
