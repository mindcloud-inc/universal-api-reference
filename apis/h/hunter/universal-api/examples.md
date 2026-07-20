# Hunter Universal API Examples

These examples use the MindCloud API key and Hunter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information?${params}`, {
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
      "calls": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "planLevel": 1,
      "planName": "Ava Chen",
      "requests": {},
      "resetDate": "string",
      "teamId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hunter/latest/actions/get-account-information).

## Add Sequence Recipient



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/add-sequence-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hunter/latest/actions/add-sequence-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
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
      "recipientsAdded": 1,
      "skippedRecipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Sequence Recipient action reference](actions/add-sequence-recipient.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hunter/latest/actions/add-sequence-recipient).
