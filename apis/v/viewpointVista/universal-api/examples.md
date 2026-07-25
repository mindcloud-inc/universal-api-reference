# Viewpoint Vista Universal API Examples

These examples use the MindCloud API key and Viewpoint Vista connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Action Instance

Vista processes write operations asynchronously. This endpoint allows the integration to confirm whether a batch or time entry was successfully created.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance?connectionId=$CONNECTION_ID&action_key_value=action-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "action_key_value": "action-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance?${params}`, {
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
      "actionCode": "string",
      "createdUtc": "string",
      "dataObjectCode": "string",
      "id": "string",
      "result": {
        "batchId": 1
      },
      "status": "string",
      "subscriberCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Action Instance action reference](actions/get-action-instance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewpointVista/latest/actions/get-action-instance).

## Add Many Time Batch Entries

Add an array of time batch entries

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-many-payroll-timecard-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].data.Co": 1,
  "items[].data.Mth": "2026-05-07T12:00:00.000Z",
  "items[].data.BatchId": 1,
  "items[].data.Employee": 1,
  "items[].data.PostDate": "2026-05-07T12:00:00.000Z",
  "items[].data.Hours": "string",
  "items[].data.TypeDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-many-payroll-timecard-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].data.Co": 1,
    "items[].data.Mth": "2026-05-07T12:00:00.000Z",
    "items[].data.BatchId": 1,
    "items[].data.Employee": 1,
    "items[].data.PostDate": "2026-05-07T12:00:00.000Z",
    "items[].data.Hours": "string",
    "items[].data.TypeDetails": {}
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

See the full [Add Many Time Batch Entries action reference](actions/add-many-payroll-timecard-entries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewpointVista/latest/actions/add-many-payroll-timecard-entries).
