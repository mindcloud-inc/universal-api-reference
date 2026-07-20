# Customer.guru Universal API Examples

These examples use the MindCloud API key and Customer.guru connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Ratings

Retrieves customer ratings from Customer.guru.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings?${params}`, {
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
      "city": "string",
      "country": "string",
      "email": "ava@example.com",
      "email_clicked_at": "2026-05-07T12:00:00.000Z",
      "email_opened_at": "2026-05-07T12:00:00.000Z",
      "email_sent_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ip_address": "string",
      "message": "string",
      "score": 1,
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Export Ratings action reference](actions/export-ratings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerguru/latest/actions/export-ratings).

## Send Survey

Creates a new survey send request in Customer.guru.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/send-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheduledFor": "now",
  "customers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/send-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scheduledFor": "now",
    "customers[]": [{}]
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
      "failed_to_send": 1,
      "status": "string",
      "successfully_sent": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Survey action reference](actions/send-survey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerguru/latest/actions/send-survey).
