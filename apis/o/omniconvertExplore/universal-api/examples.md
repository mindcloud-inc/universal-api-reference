# Omniconvert Explore Universal API Examples

These examples use the MindCloud API key and Omniconvert Explore connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Websites

Retrieves account websites from Omniconvert Explore.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/list-websites?${params}`, {
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

See the full [List Websites action reference](actions/list-websites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omniconvertExplore/latest/actions/list-websites).

## Start or Stop Experiment

Updates an experiment by starting or stopping it in Omniconvert Explore.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/start-or-stop-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "experimentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/start-or-stop-experiment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "experimentId": 1
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

See the full [Start or Stop Experiment action reference](actions/start-or-stop-experiment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omniconvertExplore/latest/actions/start-or-stop-experiment).
