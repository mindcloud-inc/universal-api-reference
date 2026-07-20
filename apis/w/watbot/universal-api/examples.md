# Watbot Universal API Examples

These examples use the MindCloud API key and Watbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves current account details from Watbot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-current-account?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/watbot/latest/actions/get-current-account).

## Add Funds To Contact Account

Adds funds to a contact account in Watbot.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-funds-to-contact-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6",
  "amount": "100",
  "description": "Stage 3 funding"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/add-funds-to-contact-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6",
    "amount": "100",
    "description": "Stage 3 funding"
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
      "amount": 1,
      "amountNote": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Funds To Contact Account action reference](actions/add-funds-to-contact-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/watbot/latest/actions/add-funds-to-contact-account).
