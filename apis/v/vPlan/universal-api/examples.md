# vPlan Universal API Examples

These examples use the MindCloud API key and vPlan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Authentication Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/retrieve-authentication-details?${params}`, {
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
      "api-key": {},
      "board_permission_set": {},
      "environment": {},
      "features": [
        "string"
      ],
      "host": {},
      "next": true,
      "settings": [
        {}
      ],
      "show_nps": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Authentication Details action reference](actions/retrieve-authentication-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vPlan/latest/actions/retrieve-authentication-details).

## Create Activity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "85b9270e-b0f4-4f8c-b492-1fb8a19c984f",
  "description": "Created through MindCloud action validation",
  "name": "Codex Action Activity"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "85b9270e-b0f4-4f8c-b492-1fb8a19c984f",
    "description": "Created through MindCloud action validation",
    "name": "Codex Action Activity"
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
      "archived_at": "string",
      "billable": true,
      "code": "string",
      "created_at": "string",
      "day_max_duration": 1,
      "default_duration": 1,
      "deleted_at": "string",
      "description": "string",
      "external_ref": "string",
      "hourly_rate": 1,
      "id": "string",
      "item_id": "string",
      "resource_type": "string",
      "transaction": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vPlan/latest/actions/create-activity).
