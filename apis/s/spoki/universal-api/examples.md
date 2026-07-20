# Spoki Universal API Examples

These examples use the MindCloud API key and Spoki connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Lists templates for the authenticated account, with optional filtering by channel-specific WABA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "customfieldSet": [
        "string"
      ],
      "id": 1,
      "integration": 1,
      "isApproved": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "subcategory": "string",
      "templateGroups": [
        {}
      ],
      "templatelocalizationSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoki/latest/actions/list-templates).

## Create Automation

Creates an automation with steps, triggers, and optional automation groups.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-automation', {
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
      "automationGroups": [
        {}
      ],
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "firstMessageText": "string",
      "id": 1,
      "isActive": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "updatedDatetime": "2026-05-07T12:00:00.000Z",
      "updatedUser": {},
      "webhookSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Automation action reference](actions/create-automation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoki/latest/actions/create-automation).
