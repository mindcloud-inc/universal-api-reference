# Planday Universal API Examples

These examples use the MindCloud API key and Planday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Portal Information

Retrieves basic portal details from Planday.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information?${params}`, {
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
      "aliases": [
        "string"
      ],
      "companyName": "Ava Chen",
      "country": "string",
      "id": 1,
      "maxDepartments": 1,
      "name": "Ava Chen",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Portal Information action reference](actions/get-portal-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planday/latest/actions/get-portal-information).

## Assign Shift

Assigns an employee to a shift in Planday.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planday/latest/actions/assign-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shiftId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/assign-shift', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shiftId": 1
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

See the full [Assign Shift action reference](actions/assign-shift.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planday/latest/actions/assign-shift).
