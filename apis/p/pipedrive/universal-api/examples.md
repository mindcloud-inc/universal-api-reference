# Pipedrive Universal API Examples

These examples use the MindCloud API key and Pipedrive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Activities

Retrieves activities from Pipedrive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?${params}`, {
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
      "addTime": "string",
      "busy": true,
      "conferenceMeetingClient": {},
      "conferenceMeetingId": {},
      "conferenceMeetingUrl": {},
      "creatorUserId": 1,
      "dealId": {},
      "done": true,
      "dueDate": "string",
      "dueTime": {},
      "duration": {},
      "id": 1,
      "isDeleted": true,
      "leadId": {},
      "location": {},
      "markedAsDoneTime": {},
      "note": {},
      "orgId": {},
      "ownerId": 1,
      "personId": {},
      "priority": {},
      "projectId": {},
      "publicDescription": {},
      "subject": "string",
      "type": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Activities action reference](actions/get-activities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedrive/latest/actions/get-activities).

## Add Activity

Creates a new activity in Pipedrive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "type": "string"
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
      "addTime": "string",
      "busy": true,
      "conferenceMeetingClient": {},
      "conferenceMeetingId": {},
      "conferenceMeetingUrl": {},
      "creatorUserId": 1,
      "dealId": {},
      "done": true,
      "dueDate": "string",
      "dueTime": {},
      "duration": {},
      "id": 1,
      "isDeleted": true,
      "leadId": {},
      "location": {},
      "markedAsDoneTime": {},
      "note": {},
      "orgId": {},
      "ownerId": 1,
      "personId": {},
      "priority": {},
      "projectId": {},
      "publicDescription": {},
      "subject": "string",
      "type": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Activity action reference](actions/add-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipedrive/latest/actions/add-activity).
