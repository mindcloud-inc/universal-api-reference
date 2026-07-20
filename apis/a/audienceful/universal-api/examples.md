# Audienceful Universal API Examples

These examples use the MindCloud API key and Audienceful connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People

Retrieves a list of people from Audienceful.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-people?${params}`, {
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
      "bounced": true,
      "clickRate": 1,
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "doubleOptIn": "string",
      "email": "ava@example.com",
      "extraData": {},
      "id": 1,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "openRate": 1,
      "source": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audienceful/latest/actions/list-people).

## Create Field

Creates a new custom field in Audienceful.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dataName": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dataName": "Ava Chen",
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
      "dataName": "Ava Chen",
      "editable": true,
      "id": "string",
      "internal": true,
      "name": "Ava Chen",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Field action reference](actions/create-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audienceful/latest/actions/create-field).
