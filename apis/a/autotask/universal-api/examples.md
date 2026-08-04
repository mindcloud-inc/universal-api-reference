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
  "amount": 1,
  "companyID": 1,
  "cost": 1,
  "ownerResourceID": 1,
  "probability": 1,
  "projectedCloseDate": "2026-05-07T12:00:00.000Z",
  "stage": 1,
  "startDate": "2026-05-07T12:00:00.000Z",
  "status": 1,
  "title": "string",
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
    "amount": 1,
    "companyID": 1,
    "cost": 1,
    "ownerResourceID": 1,
    "probability": 1,
    "projectedCloseDate": "2026-05-07T12:00:00.000Z",
    "stage": 1,
    "startDate": "2026-05-07T12:00:00.000Z",
    "status": 1,
    "title": "string",
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
