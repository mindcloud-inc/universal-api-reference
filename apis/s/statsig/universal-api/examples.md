# Statsig Universal API Examples

These examples use the MindCloud API key and Statsig connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Info

Retrieves company info from Statsig.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company?${params}`, {
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
      "companyID": "string",
      "companyName": "Ava Chen",
      "isWarehouseNative": true,
      "orgID": "string",
      "orgName": "Ava Chen",
      "resultsUpTo": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Company Info action reference](actions/get-company-info-get-console-v1-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/statsig/latest/actions/get-company-info-get-console-v1-company).

## Abandon Experiment

Abandons an experiment in Statsig.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/abandon-experiment-put-console-v1-experiments-id-abandon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "decisionReason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/abandon-experiment-put-console-v1-experiments-id-abandon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "decisionReason": "string"
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Abandon Experiment action reference](actions/abandon-experiment-put-console-v1-experiments-id-abandon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/statsig/latest/actions/abandon-experiment-put-console-v1-experiments-id-abandon).
