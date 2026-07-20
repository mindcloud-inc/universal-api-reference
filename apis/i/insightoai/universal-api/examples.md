# Insighto.ai Universal API Examples

These examples use the MindCloud API key and Insighto.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assistants



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?${params}`, {
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
      "assistant_type": "string",
      "attributes": {},
      "conversation_flow_id": "string",
      "custom_voice": true,
      "description": "string",
      "has_human_agent": true,
      "hide_ds": true,
      "id": "string",
      "llm_model": "string",
      "name": "Ava Chen",
      "org_id": "string",
      "show_images": true,
      "system_prompt": "string",
      "use_tools": true,
      "voice": true,
      "voice_languages": [
        "string"
      ],
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Assistants action reference](actions/list-assistants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightoai/latest/actions/list-assistants).

## Add Datasourcefile



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
  "dsType": "pdf",
  "datasourcefileFile": "https://example.com/file.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-datasource-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
    "dsType": "pdf",
    "datasourcefileFile": "https://example.com/file.pdf"
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
      "attributes": {},
      "description": "string",
      "ds_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "org_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Datasourcefile action reference](actions/add-datasource-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightoai/latest/actions/add-datasource-file).
