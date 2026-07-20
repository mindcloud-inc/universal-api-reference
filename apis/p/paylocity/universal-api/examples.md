# Paylocity Universal API Examples

These examples use the MindCloud API key and Paylocity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-company-information?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-company-information?${params}`, {
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

See the full [Get Company Information action reference](actions/get-company-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paylocity/latest/actions/get-company-information).

## Create Employee Punch



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/create-employee-punch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/create-employee-punch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
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

See the full [Create Employee Punch action reference](actions/create-employee-punch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paylocity/latest/actions/create-employee-punch).
