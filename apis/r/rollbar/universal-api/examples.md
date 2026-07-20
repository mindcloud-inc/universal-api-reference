# Rollbar Universal API Examples

These examples use the MindCloud API key and Rollbar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check RQL Job

Retrieves an RQL job from Rollbar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-rql-job?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-rql-job?${params}`, {
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
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Check RQL Job action reference](actions/check-rql-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rollbar/latest/actions/check-rql-job).

## Assign Team To Project

Assigns a team to a project in Rollbar.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/assign-team-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/assign-team-to-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "teamId": 1
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
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Assign Team To Project action reference](actions/assign-team-to-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rollbar/latest/actions/assign-team-to-project).
