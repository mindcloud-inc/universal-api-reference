# Click2Mail Universal API Examples

These examples use the MindCloud API key and Click2Mail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Credit Balance

Retrieves the credit balance from Click2Mail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-credit-balance?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Credit Balance action reference](actions/check-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/click2Mail/latest/actions/check-credit-balance).

## Accept Proof

Accepts a proof for a Click2Mail job.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/accept-proof" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "acceptId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/accept-proof', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "acceptId": "string"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept Proof action reference](actions/accept-proof.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/click2Mail/latest/actions/accept-proof).
