# Leave Dates Universal API Examples

These examples use the MindCloud API key and Leave Dates connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies

Retrieves companies available to the authenticated user in Leave Dates.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies?${params}`, {
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
      "allowance_unit_is_days": true,
      "billing_status": "string",
      "current_billing_plan": "string",
      "employments_count": 1,
      "id": "string",
      "minutes_per_working_day": 1,
      "name": "Ava Chen",
      "owner_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leaveDates/latest/actions/list-companies).

## Add Department

Creates a new department in Leave Dates.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "name": "Ava Chen"
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
      "company_id": "string",
      "created_at": "string",
      "id": "string",
      "is_enabled_to_see_employment_own_data": true,
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Department action reference](actions/add-department.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leaveDates/latest/actions/add-department).
