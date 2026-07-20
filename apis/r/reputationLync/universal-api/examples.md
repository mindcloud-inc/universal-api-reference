# ReputationLync Universal API Examples

These examples use the MindCloud API key and ReputationLync connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key

Validates an API key in ReputationLync.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/validate-api-key?${params}`, {
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
      "logId": 1,
      "result": "string",
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reputationLync/latest/actions/validate-api-key).

## Add Customer

Creates a new customer in ReputationLync.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/add-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/add-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Jane Doe"
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
      "customerDatesNotes": "string",
      "customerId": 1,
      "result": "string",
      "skipRatingRequest": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Customer action reference](actions/add-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reputationLync/latest/actions/add-customer).
