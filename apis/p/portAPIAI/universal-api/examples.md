# Port API AI Universal API Examples

These examples use the MindCloud API key and Port API AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Blueprints

Retrieves blueprints from Port.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-blueprints?${params}`, {
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
      "blueprints": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [List Blueprints action reference](actions/list-blueprints.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/portAPIAI/latest/actions/list-blueprints).

## Add Action Run Log

Creates an action run log in Port.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/add-action-run-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/add-action-run-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string",
    "message": "string"
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
      "ok": true,
      "runLog": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Action Run Log action reference](actions/add-action-run-log.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/portAPIAI/latest/actions/add-action-run-log).
