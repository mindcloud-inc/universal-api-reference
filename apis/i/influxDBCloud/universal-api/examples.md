# InfluxDB Cloud Universal API Examples

These examples use the MindCloud API key and InfluxDB Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buckets

Retrieves buckets from InfluxDB Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets?connectionId=$CONNECTION_ID&orgId=%7B%7Bcredentials.orgId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "{{credentials.orgId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets?${params}`, {
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
      "description": "string",
      "id": "string",
      "labels": [
        {}
      ],
      "links": {},
      "name": "Ava Chen",
      "orgID": "string",
      "retentionRules": [
        {}
      ],
      "schemaType": "string",
      "storageType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Buckets action reference](actions/list-buckets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/influxDBCloud/latest/actions/list-buckets).
