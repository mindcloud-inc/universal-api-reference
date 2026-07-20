# FreshBooks Universal API Examples

These examples use the MindCloud API key and FreshBooks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Profile

Retrieves the current user profile from FreshBooks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile?${params}`, {
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
      "businessMemberships": [
        {}
      ],
      "businessStatuses": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {}
      ],
      "id": 1,
      "identityId": 1,
      "identityOrigin": "string",
      "identityUuid": "string",
      "integrations": {},
      "language": "string",
      "lastName": "Chen",
      "links": {},
      "otpDeliveryMethod": "string",
      "otpRequiredForLogin": true,
      "permissions": {},
      "profile": {},
      "roles": [
        {}
      ],
      "setupComplete": true,
      "subscriptionStatuses": {},
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Profile action reference](actions/get-current-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshBooks/latest/actions/get-current-user-profile).

## Create Client

Creates a new client in FreshBooks for an account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
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
      "accountingSystemid": "string",
      "allowEmailIncludePdf": true,
      "allowLateFees": true,
      "allowLateNotifications": true,
      "busPhone": "string",
      "currencyCode": "string",
      "email": "ava@example.com",
      "exceedsClientLimit": 1,
      "fax": "string",
      "fname": "Ava Chen",
      "homePhone": "string",
      "id": 1,
      "language": "string",
      "level": 1,
      "lname": "Ava Chen",
      "mobPhone": "string",
      "note": "string",
      "notified": true,
      "numLogins": 1,
      "organization": "string",
      "pCity": "string",
      "pCode": "string",
      "pCountry": "string",
      "pProvince": "string",
      "prefEmail": true,
      "prefGmail": true,
      "pStreet": "string",
      "pStreet2": "string",
      "role": "string",
      "sCity": "string",
      "sCode": "string",
      "sCountry": "string",
      "signupDate": "string",
      "sProvince": "string",
      "sStreet": "string",
      "sStreet2": "string",
      "updated": "string",
      "userid": 1,
      "username": "Ava Chen",
      "uuid": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshBooks/latest/actions/create-client).
