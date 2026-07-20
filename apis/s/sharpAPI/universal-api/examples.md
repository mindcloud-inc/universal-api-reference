# SharpAPI Universal API Examples

These examples use the MindCloud API key and SharpAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Skills List

Retrieves skills from SharpAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/retrieve-skills-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/retrieve-skills-list?${params}`, {
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
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Skills List action reference](actions/retrieve-skills-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sharpAPI/latest/actions/retrieve-skills-list).

## Analyze Product Review Sentiment

Creates a product review sentiment job in SharpAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/analyze-product-review-sentiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "The performance is amazing and temps are great, but the display quality is disappointing and I will be returning it."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/analyze-product-review-sentiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "The performance is amazing and temps are great, but the display quality is disappointing and I will be returning it."
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
      "jobId": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Analyze Product Review Sentiment action reference](actions/analyze-product-review-sentiment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sharpAPI/latest/actions/analyze-product-review-sentiment).
