# Tolq Universal API Examples

These examples use the MindCloud API key and Tolq connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Translation Requests

Retrieves translation requests from Tolq.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests?${params}`, {
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
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string",
      "total_cost": 1,
      "total_keys": 1
    }
  ],
  "meta": {}
}
```

See the full [List Translation Requests action reference](actions/list-translation-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tolq/latest/actions/list-translation-requests).

## Create Quote Request

Creates a quote request in Tolq.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/create-quote-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request": "[object Object]",
  "source_language_code": "en",
  "target_language_code": "de",
  "quality": "translation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolq/latest/actions/create-quote-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request": "[object Object]",
    "source_language_code": "en",
    "target_language_code": "de",
    "quality": "translation"
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
      "_links": {},
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "quality": "string",
      "slug": "string",
      "source_language_code": "string",
      "status": "string",
      "style_guide_reference_id": 1,
      "target_language_code": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Quote Request action reference](actions/create-quote-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tolq/latest/actions/create-quote-request).
