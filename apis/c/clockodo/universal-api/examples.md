# Clockodo Universal API Examples

These examples use the MindCloud API key and Clockodo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Services

Retrieves services from your Clockodo account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/list-services?${params}`, {
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
      "active": true,
      "billableDefault": true,
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "number": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Services action reference](actions/list-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clockodo/latest/actions/list-services).

## Change Duration

Updates the clock duration in your Clockodo account.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/change-duration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "durationBefore": 1,
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockodo/latest/actions/change-duration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "durationBefore": 1,
    "duration": 1
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
      "billable": 1,
      "budgetType": "string",
      "calcAlsoRevenuesForProjectsWithHardBudget": true,
      "customersId": "string",
      "duration": 1,
      "enhancedList": true,
      "hourlyRate": 1,
      "id": "string",
      "lumpsum": 1,
      "lumpsumServicesAmount": 1,
      "lumpsumServicesId": "string",
      "projectsId": "string",
      "servicesId": "string",
      "text": "string",
      "textsId": "string",
      "timeSince": "string",
      "timeUntil": "string",
      "usersId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Duration action reference](actions/change-duration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clockodo/latest/actions/change-duration).
