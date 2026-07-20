# TravelPerk Universal API Examples

These examples use the MindCloud API key and TravelPerk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Invoice Lines

Retrieves invoice lines from TravelPerk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines?${params}`, {
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
      "invoice_lines": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Invoice Lines action reference](actions/list-invoice-lines.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/travelPerk/latest/actions/list-invoice-lines).

## Assign Users to Cost Center

Assigns users to a cost center in TravelPerk.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/assign-users-to-cost-center" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "costCenterId": "string",
  "user_ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/assign-users-to-cost-center', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "costCenterId": "string",
    "user_ids[]": ["string"]
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
      "approver": {},
      "approver_id": "string",
      "archived": true,
      "count_users": 1,
      "delegate": {},
      "delegate_expiry": "string",
      "delegate_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Assign Users to Cost Center action reference](actions/assign-users-to-cost-center.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/travelPerk/latest/actions/assign-users-to-cost-center).
