# Influencers.club Universal API Examples

These examples use the MindCloud API key and Influencers.club connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account Credits And Usage

Retrieves account credits and usage details from Influencers.club.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage?${params}`, {
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
      "credits_available": 1,
      "credits_used": 1
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account Credits And Usage action reference](actions/retrieve-account-credits-and-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/influencersclub/latest/actions/retrieve-account-credits-and-usage).

## Create Enrichment Batch

Creates a batch enrichment job in Influencers.club from a CSV.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/create-enrichment-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "enrichmentMode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/create-enrichment-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "enrichmentMode": "string"
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
      "batch_id": "string",
      "created_at": "string",
      "enrichment_mode": "string",
      "message": "string",
      "metadata": {},
      "og_input_number": 1,
      "platform": "string",
      "status": "string",
      "type_report": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Enrichment Batch action reference](actions/create-enrichment-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/influencersclub/latest/actions/create-enrichment-batch).
