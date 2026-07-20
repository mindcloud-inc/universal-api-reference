# Instantly Universal API Examples

These examples use the MindCloud API key and Instantly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Workspace

Retrieves the current workspace from Instantly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "planId": "string",
      "planIdLeadfinder": "string",
      "timestampCreated": "string",
      "timestampUpdated": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Workspace action reference](actions/get-current-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instantly/latest/actions/get-current-workspace).

## Activate Campaign

Activates a campaign in Instantly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/activate-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/activate-campaign', {
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
      "campaign_schedule": {},
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
      "timestamp_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Activate Campaign action reference](actions/activate-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instantly/latest/actions/activate-campaign).
