# Teamdeck Universal API Examples

These examples use the MindCloud API key and Teamdeck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization

Retrieves your organization details from Teamdeck.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-organization?${params}`, {
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
      "disableVacationApproval": 1,
      "name": "Ava Chen",
      "workWeek": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamdeck/latest/actions/get-organization).

## Activate Resource

Activates an existing resource in Teamdeck.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/activate-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/activate-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "active": true,
      "avatar": "string",
      "canSeeCalendar": true,
      "contractEndDate": "string",
      "contractStartDate": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "isPartTime": true,
      "isVisible": true,
      "name": "Ava Chen",
      "organizationUnitId": 1,
      "role": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Resource action reference](actions/activate-resource.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamdeck/latest/actions/activate-resource).
