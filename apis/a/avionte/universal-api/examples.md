# Avionte Universal API Examples

These examples use the MindCloud API key and Avionte connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Branches

Retrieves branches from Avionte.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-branches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-branches?${params}`, {
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

See the full [Get Branches action reference](actions/get-branches.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avionte/latest/actions/get-branches).

## Add Talent to Pipeline Stage



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/add-talent-to-pipeline-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobActivityName": "Ava Chen",
  "jobId": "string",
  "talentId": "string",
  "stageType": "string",
  "stagedDate": "string",
  "jobActivityDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avionte/latest/actions/add-talent-to-pipeline-stage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobActivityName": "Ava Chen",
    "jobId": "string",
    "talentId": "string",
    "stageType": "string",
    "stagedDate": "string",
    "jobActivityDate": "string"
  })
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

See the full [Add Talent to Pipeline Stage action reference](actions/add-talent-to-pipeline-stage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avionte/latest/actions/add-talent-to-pipeline-stage).
