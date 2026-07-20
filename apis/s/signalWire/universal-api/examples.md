# SignalWire Universal API Examples

These examples use the MindCloud API key and SignalWire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Fabric Resources

Retrieves Fabric resources from SignalWire.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fabric-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fabric-resources?${params}`, {
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
      "ai_agent": {
        "agent_id": "string",
        "name": "Ava Chen",
        "params": {
          "acknowledge_interruptions": true,
          "ai_name": "Ava Chen",
          "ai_volume": 1,
          "app_name": "Ava Chen",
          "attention_timeout": 1,
          "attention_timeout_prompt": "string",
          "background_file": "string",
          "background_file_loops": 1,
          "background_file_volume": 1,
          "barge_match_string": "string",
          "barge_min_words": 1,
          "conscience": "string",
          "conversation_id": "string",
          "convo": [
            {}
          ],
          "debug": true,
          "debug_webhook_level": 1,
          "debug_webhook_url": "https://example.com",
          "digit_termiantors": "string",
          "direction": [
            "string"
          ]
        },
        "post_prompt": {
          "confidence": 1,
          "frequency_penalty": 1,
          "presence_penalty": 1,
          "temperature": 1,
          "text": "string",
          "top_p": 1
        },
        "prompt": {
          "confidence": 1,
          "contexts": {
            "default": {
              "steps": [
                {}
              ]
            }
          },
          "frequency_penalty": 1,
          "presence_penalty": 1,
          "temperature": 1,
          "text": "string",
          "top_p": 1
        }
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Fabric Resources action reference](actions/list-fabric-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signalWire/latest/actions/list-fabric-resources).

## Assign a resource as a call handler for a Domain Application.

Assigns a resource as a call handler for a domain application in SignalWire.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "domainApplicationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "domainApplicationId": "string"
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
      "channels": {
        "audio": "string"
      },
      "cover_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "locked": true,
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign a resource as a call handler for a Domain Application. action reference](actions/assign-a-resource-as-a-call-handler-for-a-domain-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signalWire/latest/actions/assign-a-resource-as-a-call-handler-for-a-domain-application).
