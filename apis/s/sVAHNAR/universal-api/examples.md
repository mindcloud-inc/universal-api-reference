# SVAHNAR Universal API Examples

These examples use the MindCloud API key and SVAHNAR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Agent Configuration

Retrieves an agent configuration from SVAHNAR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-configuration?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-configuration?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Agent Configuration action reference](actions/get-agent-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sVAHNAR/latest/actions/get-agent-configuration).

## Run Agent

Runs an agent in SVAHNAR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/run-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/run-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
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
      "additional_metadata": {},
      "request_metadata": {},
      "response": [
        {}
      ],
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Run Agent action reference](actions/run-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sVAHNAR/latest/actions/run-agent).
