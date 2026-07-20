# Polymer Universal API Examples

These examples use the MindCloud API key and Polymer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Candidate

Retrieves a candidate from Polymer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polymer/latest/actions/get-candidate?${params}`, {
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

See the full [Get Candidate action reference](actions/get-candidate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/polymer/latest/actions/get-candidate).

## Apply For Job

Applies a candidate to a job in Polymer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/apply-for-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polymer/latest/actions/apply-for-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Apply For Job action reference](actions/apply-for-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/polymer/latest/actions/apply-for-job).
