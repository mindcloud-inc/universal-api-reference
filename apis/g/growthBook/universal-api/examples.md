# GrowthBook Universal API Examples

These examples use the MindCloud API key and GrowthBook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all projects

Retrieves projects from your GrowthBook organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-projects?${params}`, {
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
      "count": 1,
      "hasMore": true,
      "limit": 1,
      "nextOffset": 1,
      "offset": 1,
      "projects": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get all projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/growthBook/latest/actions/list-projects).

## Add a target rule to a ramp schedule

Adds a target rule to a GrowthBook ramp schedule.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/add-target-ramp-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "featureId": "sample_id_1",
  "ruleId": "rule_1",
  "environment": "production"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/add-target-ramp-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "featureId": "sample_id_1",
    "ruleId": "rule_1",
    "environment": "production"
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
      "rampSchedule": {}
    }
  ],
  "meta": {}
}
```

See the full [Add a target rule to a ramp schedule action reference](actions/add-target-ramp-schedule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/growthBook/latest/actions/add-target-ramp-schedule).
