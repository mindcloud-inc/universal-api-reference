# Matomo Universal API Examples

These examples use the MindCloud API key and Matomo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Matomo Version



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-matomo-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-matomo-version?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Matomo Version action reference](actions/get-matomo-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/matomo/latest/actions/get-matomo-version).

## AbTesting add Experiment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/ab-testing-add-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idSite": "1",
  "name": "Ava Chen",
  "hypothesis": "string",
  "description": "string",
  "variations": "string",
  "includedTargets": "string",
  "successMetrics": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/ab-testing-add-experiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idSite": "1",
    "name": "Ava Chen",
    "hypothesis": "string",
    "description": "string",
    "variations": "string",
    "includedTargets": "string",
    "successMetrics": "string"
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
      "label": "string",
      "nb_actions": 1,
      "nb_uniq_visitors": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [AbTesting add Experiment action reference](actions/ab-testing-add-experiment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/matomo/latest/actions/ab-testing-add-experiment).
