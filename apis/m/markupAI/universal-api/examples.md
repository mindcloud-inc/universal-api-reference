# Markup AI Universal API Examples

These examples use the MindCloud API key and Markup AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Style Guides

Retrieves style guides from Markup AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides?${params}`, {
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
      "base_style_guide_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "has_tone_prompt": true,
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "summary": "string",
      "terminology_domain_ids": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Style Guides action reference](actions/list-style-guides.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/markupAI/latest/actions/list-style-guides).

## Create Domain

Creates a new terminology domain in Markup AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "term_set_count": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Domain action reference](actions/create-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/markupAI/latest/actions/create-domain).
