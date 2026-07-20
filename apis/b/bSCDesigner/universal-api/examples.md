# BSC Designer Universal API Examples

These examples use the MindCloud API key and BSC Designer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Request Count Limit Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info?${params}`, {
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
      "allowedCount": 1,
      "email": "ava@example.com",
      "error": {},
      "usedCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Request Count Limit Info action reference](actions/get-request-count-limit-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bSCDesigner/latest/actions/get-request-count-limit-info).

## Balance Scorecard



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/balance-scorecard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/balance-scorecard', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string"
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
      "indicatorGuid": "string",
      "indicatorName": "Ava Chen",
      "newWeight": 1,
      "oldWeight": 1
    }
  ],
  "meta": {}
}
```

See the full [Balance Scorecard action reference](actions/balance-scorecard.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bSCDesigner/latest/actions/balance-scorecard).
