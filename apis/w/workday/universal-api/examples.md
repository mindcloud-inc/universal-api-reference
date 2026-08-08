# Workday Universal API Examples

These examples use the MindCloud API key and Workday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workers

List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?${params}`, {
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
      "additionalJobs": [
        {}
      ],
      "descriptor": "string",
      "id": "string",
      "person": {},
      "primaryJob": {},
      "workerId": "string",
      "workerType": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Workers action reference](actions/get-workers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workday/latest/actions/get-workers).
