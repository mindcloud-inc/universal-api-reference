# updown.io Universal API Examples

These examples use the MindCloud API key and updown.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Checks

Retrieves all monitoring checks from updown.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-checks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-checks?${params}`, {
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
      "alias": "string",
      "apdex_t": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_headers": {},
      "disabled_locations": [
        "string"
      ],
      "domain": {},
      "down": true,
      "down_since": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "error": "string",
      "favicon_url": "https://example.com",
      "http_body": "string",
      "http_verb": "string",
      "last_check_at": "2026-05-07T12:00:00.000Z",
      "last_status": 1,
      "mute_until": "2026-05-07T12:00:00.000Z",
      "next_check_at": "2026-05-07T12:00:00.000Z",
      "period": 1,
      "published": true,
      "recipients": [
        "string"
      ],
      "string_match": "string",
      "token": "string",
      "type": "string",
      "up_since": "2026-05-07T12:00:00.000Z",
      "uptime": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Checks action reference](actions/list-checks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/updownio/latest/actions/list-checks).

## Create Check

Creates a new check in updown.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "alias": "string",
      "apdex_t": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_headers": {},
      "disabled_locations": [
        "string"
      ],
      "down": true,
      "down_since": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "error": "string",
      "favicon_url": "https://example.com",
      "http_body": "string",
      "http_verb": "string",
      "last_check_at": "2026-05-07T12:00:00.000Z",
      "last_status": 1,
      "mute_until": "2026-05-07T12:00:00.000Z",
      "next_check_at": "2026-05-07T12:00:00.000Z",
      "period": 1,
      "published": true,
      "recipients": [
        "string"
      ],
      "string_match": "string",
      "token": "string",
      "type": "string",
      "up_since": "2026-05-07T12:00:00.000Z",
      "uptime": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Check action reference](actions/create-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/updownio/latest/actions/create-check).
