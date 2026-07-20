# HoneyHive Universal API Examples

These examples use the MindCloud API key and HoneyHive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Projects

Retrieves a list of projects from HoneyHive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-projects?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Projects action reference](actions/get-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/honeyHive/latest/actions/get-projects).

## Add Datapoints

Adds datapoints to a dataset in HoneyHive.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/add-datapoints" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "project": "string",
  "data[]": [
    {}
  ],
  "mapping": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/add-datapoints', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "project": "string",
    "data[]": [{}],
    "mapping": {}
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
      "datapointIds": [
        "string"
      ],
      "inserted": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Datapoints action reference](actions/add-datapoints.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/honeyHive/latest/actions/add-datapoints).
