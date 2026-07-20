# CallScaler Universal API Examples

These examples use the MindCloud API key and CallScaler connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calls

Retrieves calls from CallScaler.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-calls?${params}`, {
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
      "ai_category": "string",
      "ai_score": 1,
      "call_flow_name": "Ava Chen",
      "caller_name": "Ava Chen",
      "caller_number": "string",
      "cost_cents": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_number": "string",
      "direction": "string",
      "duration_seconds": 1,
      "has_transcription": true,
      "id": "string",
      "keywords_spotted": [
        [
          "string"
        ]
      ],
      "qualification_reason": "string",
      "qualified_ai": true,
      "recording_duration": 1,
      "recording_url": "https://example.com",
      "robo_score": 1,
      "source": "string",
      "status": "string",
      "tracking_number": "string",
      "utm_campaign": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "value_cents": 1
    }
  ],
  "meta": {}
}
```

See the full [List Calls action reference](actions/list-calls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callScaler/latest/actions/list-calls).

## Add Number Group Members

Updates a number group in CallScaler by adding members.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/add-number-group-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/add-number-group-members', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Number Group Members action reference](actions/add-number-group-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callScaler/latest/actions/add-number-group-members).
