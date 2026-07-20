# SMSup Universal API Examples

These examples use the MindCloud API key and SMSup connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance?${params}`, {
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
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSup/latest/actions/get-account-balance).

## Add Subaccount Balance



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/add-subaccount-balance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userName": "subaccount_user_name",
  "amount": "150"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/add-subaccount-balance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userName": "subaccount_user_name",
    "amount": "150"
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
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Subaccount Balance action reference](actions/add-subaccount-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSup/latest/actions/add-subaccount-balance).
