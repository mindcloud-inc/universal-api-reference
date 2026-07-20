# Zapier NLA Universal API Examples

These examples use the MindCloud API key and Zapier NLA connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/check-connection?${params}`, {
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
      "email": "ava@example.com",
      "success": true,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Connection action reference](actions/check-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zapierNLA/latest/actions/check-connection).

## Execute Dynamic Exposed Action



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/execute-dynamic-exposed-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "exposed_app_action_id": "string",
  "instructions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/execute-dynamic-exposed-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "exposed_app_action_id": "string",
    "instructions": "string"
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
      "action_used": "string",
      "additional_results": [
        {}
      ],
      "assistant_hint": "string",
      "error": "string",
      "id": "string",
      "input_params": {},
      "result": {},
      "result_field_labels": {},
      "review_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Execute Dynamic Exposed Action action reference](actions/execute-dynamic-exposed-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zapierNLA/latest/actions/execute-dynamic-exposed-action).
