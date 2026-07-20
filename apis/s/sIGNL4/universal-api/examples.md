# SIGNL4 Universal API Examples

These examples use the MindCloud API key and SIGNL4 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from SIGNL4.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-teams?${params}`, {
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
      "description": "string",
      "externalName": "Ava Chen",
      "id": "string",
      "imageLastModified": "2026-05-07T12:00:00.000Z",
      "imageWebLastModified": "2026-05-07T12:00:00.000Z",
      "memberIds": [
        "string"
      ],
      "name": "Ava Chen",
      "options": 1,
      "subscriptionId": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sIGNL4/latest/actions/list-teams).

## Acknowledge Alert

Updates an alert as acknowledged in SIGNL4.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/acknowledge-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertId": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/acknowledge-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertId": "string",
    "uid": "string"
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
      "alertingPatternId": "string",
      "alertingPatternName": "Ava Chen",
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "eventDistributionId": "string",
      "eventDistributionName": "Ava Chen",
      "eventId": "string",
      "eventSourceId": "string",
      "externalId": "string",
      "flags": 1,
      "history": {
        "acknowledgedAt": "2026-05-07T12:00:00.000Z",
        "acknowledgements": [
          "string"
        ],
        "closedAt": "2026-05-07T12:00:00.000Z",
        "closedBy": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "createdBy": "string",
        "createdByName": "Ava Chen"
      },
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "requiredAcknowledgements": 1,
      "severity": 1,
      "status": {},
      "subscriptionId": "string",
      "teamId": "string",
      "text": "string",
      "title": "string",
      "workflowType": 1
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Alert action reference](actions/acknowledge-alert.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sIGNL4/latest/actions/acknowledge-alert).
