# Enrich.so Universal API Examples

These examples use the MindCloud API key and Enrich.so connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves credit balance from Enrich.so.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance?${params}`, {
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
      "credits_remaining": 1,
      "credits_used": 1,
      "team": "string",
      "total_credits": 1,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/enrich/latest/actions/get-credit-balance).

## Find Emails in Batch

Creates a batch email finder job in Enrich.so.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-emails-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leads[]": [
    {
      "domain": "stripe.com",
      "lastName": "Chen",
      "firstName": "Sarah"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-emails-in-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leads[]": [{"domain":"stripe.com","lastName":"Chen","firstName":"Sarah"}]
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
      "batchId": "string",
      "duplicatesRemoved": 1,
      "itemCount": 1,
      "originalCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Find Emails in Batch action reference](actions/find-emails-in-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/enrich/latest/actions/find-emails-in-batch).
