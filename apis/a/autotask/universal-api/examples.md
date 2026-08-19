# Autotask Universal API Examples

These examples use the MindCloud API key and Autotask connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection?${params}`, {
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
      "build": "string",
      "customerType": "string",
      "majorVersion": "string",
      "minorVersion": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autotask/latest/actions/test-connection).

## Create Opportunity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "12345",
  "title": "Managed services renewal",
  "ownerResourceId": "12345",
  "amount": "0",
  "cost": "0",
  "probability": "50",
  "projectedCloseDate": "2026-09-30",
  "stage": "1",
  "status": "1",
  "useQuoteTotals": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-opportunity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "12345",
    "title": "Managed services renewal",
    "ownerResourceId": "12345",
    "amount": "0",
    "cost": "0",
    "probability": "50",
    "projectedCloseDate": "2026-09-30",
    "stage": "1",
    "status": "1",
    "useQuoteTotals": true
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

See the full [Create Opportunity action reference](actions/create-opportunity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autotask/latest/actions/create-opportunity).
