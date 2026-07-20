# Pingueen Universal API Examples

These examples use the MindCloud API key and Pingueen connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients?${params}`, {
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
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "ds_address": "string",
      "ds_name": "Ava Chen",
      "ds_phone": "string",
      "ds_surname": "Ava Chen",
      "dt_last_message": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "is_enabled": true,
      "is_suspended": true,
      "last_message": "string",
      "manual_assignees": [
        {}
      ],
      "meta_info": [
        {}
      ],
      "opt_in": {},
      "read_later": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingueen/latest/actions/list-clients).

## Assign Client Agents



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/assign-client-agents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agents[]": [
    {}
  ],
  "agents[].agent": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/assign-client-agents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agents[]": [{}],
    "agents[].agent": "string",
    "id": "string"
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
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Assign Client Agents action reference](actions/assign-client-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingueen/latest/actions/assign-client-agents).
