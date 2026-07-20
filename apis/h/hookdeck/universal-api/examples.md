# Hookdeck Universal API Examples

These examples use the MindCloud API key and Hookdeck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Connections

Retrieves connections from Hookdeck.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destination": {},
      "disabled_at": "2026-05-07T12:00:00.000Z",
      "full_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "paused_at": "2026-05-07T12:00:00.000Z",
      "rules": [
        {}
      ],
      "source": {},
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Connections action reference](actions/get-connections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hookdeck/latest/actions/get-connections).

## Cancel Event

Cancels a pending event in Hookdeck.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/cancel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/cancel-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
      "attempts": 1,
      "cli_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "destination_id": "string",
      "error_code": "string",
      "event_data_id": "string",
      "id": "string",
      "last_attempt_at": "2026-05-07T12:00:00.000Z",
      "next_attempt_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "response_status": 1,
      "source_id": "string",
      "status": "string",
      "successful_at": "2026-05-07T12:00:00.000Z",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Event action reference](actions/cancel-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hookdeck/latest/actions/cancel-event).
