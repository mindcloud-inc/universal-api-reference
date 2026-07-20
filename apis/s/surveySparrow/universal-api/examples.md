# SurveySparrow Universal API Examples

These examples use the MindCloud API key and SurveySparrow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Translation

Retrieves a translation Excel file from SurveySparrow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/export-translation?connectionId=$CONNECTION_ID&surveyId=1&languageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "languageCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/export-translation?${params}`, {
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
      "translation_file": "string"
    }
  ],
  "meta": {}
}
```

See the full [Export Translation action reference](actions/export-translation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/surveySparrow/latest/actions/export-translation).

## Create Audit Log Event

Creates a subscribed audit log event in SurveySparrow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-audit-log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    {}
  ],
  "httpMethod": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-audit-log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": [{}],
    "httpMethod": "string",
    "url": "https://example.com"
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
      "events": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Audit Log Event action reference](actions/create-audit-log-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/surveySparrow/latest/actions/create-audit-log-event).
