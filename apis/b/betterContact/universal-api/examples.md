# BetterContact Universal API Examples

These examples use the MindCloud API key and BetterContact connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Credit Balance

Retrieves the current BetterContact credit balance and account email.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance?${params}`, {
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
      "creditsLeft": "string",
      "email": "ava@example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Check Credit Balance action reference](actions/check-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterContact/latest/actions/check-credit-balance).

## Create Enrichment

Creates an asynchronous BetterContact contact enrichment request.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Elon",
  "lastName": "Musk",
  "company": "Tesla",
  "enrichEmailAddress": "true",
  "enrichPhoneNumber": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-enrichment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Elon",
    "lastName": "Musk",
    "company": "Tesla",
    "enrichEmailAddress": "true",
    "enrichPhoneNumber": "false"
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
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Enrichment action reference](actions/create-enrichment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/betterContact/latest/actions/create-enrichment).
