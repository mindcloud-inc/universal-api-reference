# Metronome Universal API Examples

These examples use the MindCloud API key and Metronome connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Metronome.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-customers?${params}`, {
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
      "external_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metronome/latest/actions/list-customers).

## Create Billable Metric

Creates a new billable metric in Metronome.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-billable-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "aggregationType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-billable-metric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "aggregationType": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Billable Metric action reference](actions/create-billable-metric.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/metronome/latest/actions/create-billable-metric).
