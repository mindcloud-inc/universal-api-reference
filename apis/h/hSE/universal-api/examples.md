# 4HSE Universal API Examples

These examples use the MindCloud API key and 4HSE connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Action Sessions

Retrieves action sessions from 4HSE.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?${params}`, {
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
      "actionId": "string",
      "actionName": "Ava Chen",
      "actionSessionId": "string",
      "actionType": "string",
      "dateBegin": "2026-05-07T12:00:00.000Z",
      "dateExpire": "2026-05-07T12:00:00.000Z",
      "officeName": "Ava Chen",
      "permission": "string",
      "subtenantId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Action Sessions action reference](actions/list-action-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hSE/latest/actions/list-action-sessions).

## Assign Person To Work Group

Creates a new work group assignment in 4HSE.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/assign-person-to-work-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workGroupId": "string",
  "personOfficeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/assign-person-to-work-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workGroupId": "string",
    "personOfficeId": "string"
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

See the full [Assign Person To Work Group action reference](actions/assign-person-to-work-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hSE/latest/actions/assign-person-to-work-group).
