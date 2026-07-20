# TelTel Universal API Examples

These examples use the MindCloud API key and TelTel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance

Retrieves account balance details from your TelTel account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance?${params}`, {
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
      "balance": 1,
      "credit": 1,
      "creditLimit": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/telTel/latest/actions/get-account-balance).

## Assign Phone Number To Groups

Assigns a phone number to groups in TelTel.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/assign-phone-number-to-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/telTel/latest/actions/assign-phone-number-to-groups', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "groups": [
        {}
      ],
      "id": 1,
      "phoneNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Phone Number To Groups action reference](actions/assign-phone-number-to-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/telTel/latest/actions/assign-phone-number-to-groups).
