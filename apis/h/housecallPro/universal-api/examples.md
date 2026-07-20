# Housecall Pro Universal API Examples

These examples use the MindCloud API key and Housecall Pro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers?${params}`, {
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
      "addresses": [
        {}
      ],
      "company": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homeNumber": "string",
      "id": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "mobileNumber": "string",
      "notes": "string",
      "notificationsEnabled": true,
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/housecallPro/latest/actions/list-customers).

## Bulk Update Estimate Option Line Items



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/bulk-update-estimate-option-line-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimateId": "csr_48c56f1d6e304fd3bd64069968d58d3b",
  "optionId": "est_4c3bbad072de4216a21da7918c8e5854",
  "lineItems[].name": "Diagnostic Add-on"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/bulk-update-estimate-option-line-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimateId": "csr_48c56f1d6e304fd3bd64069968d58d3b",
    "optionId": "est_4c3bbad072de4216a21da7918c8e5854",
    "lineItems[].name": "Diagnostic Add-on"
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
      "data": [
        {}
      ],
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Estimate Option Line Items action reference](actions/bulk-update-estimate-option-line-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/housecallPro/latest/actions/bulk-update-estimate-option-line-items).
