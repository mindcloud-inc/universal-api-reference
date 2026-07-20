# Agilite Universal API Examples

These examples use the MindCloud API key and Agilite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Active BPM Steps

Retrieves active BPM steps from Agilite by process key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-active-bpm-steps?connectionId=$CONNECTION_ID&processKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-active-bpm-steps?${params}`, {
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

See the full [Get Active BPM Steps action reference](actions/get-active-bpm-steps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agilite/latest/actions/get-active-bpm-steps).

## Assign BPM Role

Assigns a role to a BPM record in Agilite.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/assign-bpm-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bpmRecordId": "string",
  "currentUser": "string",
  "roleName": "Ava Chen",
  "responsibleUsers": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/assign-bpm-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bpmRecordId": "string",
    "currentUser": "string",
    "roleName": "Ava Chen",
    "responsibleUsers": "string"
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

See the full [Assign BPM Role action reference](actions/assign-bpm-role.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agilite/latest/actions/assign-bpm-role).
