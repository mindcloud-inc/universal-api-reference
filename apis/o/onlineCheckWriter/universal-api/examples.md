# OnlineCheckWriter Universal API Examples

These examples use the MindCloud API key and OnlineCheckWriter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Wallets

Lists wallets available in the connected OnlineCheckWriter account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/list-wallets?${params}`, {
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
      "data": [
        {
          "availableBalance": "string",
          "bankAccountId": {},
          "bankAccountName": {},
          "bankAccountNatureType": {},
          "bankAccountNickName": {},
          "bankAccountNumber": "string",
          "currentBalance": "string",
          "id": "string",
          "walletName": "Ava Chen",
          "walletType": 1
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "perPage": 1,
        "total": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Wallets action reference](actions/list-wallets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onlineCheckWriter/latest/actions/list-wallets).

## Create Bank Accounts

Creates up to 20 bank accounts in a single request.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/create-bank-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/create-bank-accounts', {
  method: 'POST',
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
  "data": [],
  "meta": {}
}
```

See the full [Create Bank Accounts action reference](actions/create-bank-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onlineCheckWriter/latest/actions/create-bank-accounts).
