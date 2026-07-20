# FreeAgent Universal API Examples

These examples use the MindCloud API key and FreeAgent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bill

Retrieves detailed bill information from FreeAgent.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill?${params}`, {
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
      "comments": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "due_on": "2026-05-07T12:00:00.000Z",
      "due_value": "string",
      "input_total_values_inc_tax": true,
      "is_locked": true,
      "is_paid_by_hire_purchase": true,
      "long_status": "string",
      "native_due_value": "string",
      "net_value": "string",
      "paid_value": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Bill action reference](actions/get-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freeAgent/latest/actions/get-bill).

## Create Bill

Creates a new bill in FreeAgent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bill.contact": "string",
  "bill.reference": "string",
  "bill.dated_on": "2026-05-07T12:00:00.000Z",
  "bill.due_on": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bill.contact": "string",
    "bill.reference": "string",
    "bill.dated_on": "2026-05-07T12:00:00.000Z",
    "bill.due_on": "2026-05-07T12:00:00.000Z"
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
      "comments": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "due_on": "2026-05-07T12:00:00.000Z",
      "due_value": "string",
      "input_total_values_inc_tax": true,
      "is_locked": true,
      "is_paid_by_hire_purchase": true,
      "long_status": "string",
      "native_due_value": "string",
      "net_value": "string",
      "paid_value": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Bill action reference](actions/create-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freeAgent/latest/actions/create-bill).
