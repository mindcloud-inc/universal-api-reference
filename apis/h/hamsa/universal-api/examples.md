# Hamsa Universal API Examples

These examples use the MindCloud API key and Hamsa connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project By API Key

Retrieves a project from Hamsa by API key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-project-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-project-by-api-key?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isDeactivated": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Project By API Key action reference](actions/get-project-by-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hamsa/latest/actions/get-project-by-api-key).

## Assign Phone Number to Voice Agent

Assigns a phone number to a Hamsa voice agent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/assign-phone-number-to-voice-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "voiceAgentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/assign-phone-number-to-voice-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "voiceAgentId": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "label": "string",
      "number": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "voiceAgentId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Phone Number to Voice Agent action reference](actions/assign-phone-number-to-voice-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hamsa/latest/actions/assign-phone-number-to-voice-agent).
