# ADP Universal API Examples

These examples use the MindCloud API key and ADP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Business Units

Associate Business Units

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Business Units action reference](actions/list-business-units.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adp/latest/actions/list-business-units).

## Create Payroll Batch



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-payroll-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyCode": "string",
  "batchID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-payroll-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyCode": "string",
    "batchID": "string"
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

See the full [Create Payroll Batch action reference](actions/create-payroll-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/adp/latest/actions/create-payroll-batch).
