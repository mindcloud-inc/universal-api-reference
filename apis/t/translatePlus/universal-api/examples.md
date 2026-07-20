# TranslatePlus Universal API Examples

These examples use the MindCloud API key and TranslatePlus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Summary

Retrieves account summary and credit usage from TranslatePlus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary?${params}`, {
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
      "concurrency": 1,
      "credits_percentage": 1,
      "credits_remaining": 1,
      "credits_used": 1,
      "effective_concurrency": 1,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "summary": {},
      "total_credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Summary action reference](actions/get-account-summary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/translatePlus/latest/actions/get-account-summary).

## Batch Translate Text

Translates multiple texts in one TranslatePlus request.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/batch-translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "texts[]": [
    "string"
  ],
  "source": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/batch-translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "texts[]": ["string"],
    "source": "string",
    "target": "string"
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
      "failed": 1,
      "successful": 1,
      "total": 1,
      "translations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Translate Text action reference](actions/batch-translate-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/translatePlus/latest/actions/batch-translate-text).
