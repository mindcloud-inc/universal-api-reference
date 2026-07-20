# Privy Universal API Examples

These examples use the MindCloud API key and Privy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from Privy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users?${params}`, {
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
          "created_at": 1,
          "custom_metadata": {},
          "has_accepted_terms": true,
          "id": "string",
          "is_guest": true,
          "linked_accounts": [
            {
              "address": "https://example.com",
              "type": "https://example.com"
            }
          ]
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/privy/latest/actions/list-users).

## Authenticate Wallet

Authenticates a wallet session in Privy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/authenticate-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/authenticate-wallet', {
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
  "data": [
    {
      "encrypted_authorization_key": {
        "ciphertext": "string",
        "encapsulated_key": "string",
        "encryption_type": "string"
      },
      "expires_at": 1,
      "wallets": [
        {
          "address": "string",
          "chain_type": "string",
          "created_at": 1,
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Authenticate Wallet action reference](actions/authenticate-wallet.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/privy/latest/actions/authenticate-wallet).
