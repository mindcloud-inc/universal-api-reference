# Verifalia Universal API Examples

These examples use the MindCloud API key and Verifalia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits Balance

Retrieves the current credits balance from Verifalia.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance?${params}`, {
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
      "creditPacks": 1,
      "freeCredits": 1,
      "freeCreditsResetIn": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credits Balance action reference](actions/get-credits-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verifalia/latest/actions/get-credits-balance).

## Activate Contact Method

Activates a contact method in Verifalia.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/activate-contact-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "contactMethodId": "string",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/activate-contact-method', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "contactMethodId": "string",
    "code": "string"
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

See the full [Activate Contact Method action reference](actions/activate-contact-method.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verifalia/latest/actions/activate-contact-method).
