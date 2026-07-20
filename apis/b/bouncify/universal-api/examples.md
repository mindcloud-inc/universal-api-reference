# Bouncify Universal API Examples

These examples use the MindCloud API key and Bouncify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves credit balance information from Bouncify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance?${params}`, {
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
      "creditsInfo": {
        "creditsRemaining": 1,
        "paygCredit": 1,
        "subscriptionCredit": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bouncify/latest/actions/get-credit-balance).

## Start Verifying Bulk List

Starts verifying a bulk email list in Bouncify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/start-verifying-bulk-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/start-verifying-bulk-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
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
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Start Verifying Bulk List action reference](actions/start-verifying-bulk-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bouncify/latest/actions/start-verifying-bulk-list).
