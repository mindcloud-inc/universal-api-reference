# Billit Universal API Examples

These examples use the MindCloud API key and Billit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves account information for the authenticated Billit user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information?${params}`, {
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
      "Companies": [
        {}
      ],
      "Email": "ava@example.com",
      "LoginOrRegisterNeeded": true,
      "UserCompanyRoles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billit/latest/actions/get-account-information).

## Create Party

Creates a new party in Billit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen",
  "PartyType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-party', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen",
    "PartyType": "string"
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
      "data": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Party action reference](actions/create-party.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billit/latest/actions/create-party).
