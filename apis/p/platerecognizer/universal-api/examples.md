# Platerecognizer Universal API Examples

These examples use the MindCloud API key and Platerecognizer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Statistics

Retrieves your Plate Recognizer Snapshot usage statistics.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-statistics?${params}`, {
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
      "totalCalls": 1,
      "usage": {
        "calls": 1,
        "month": 1,
        "resetsOn": "2026-05-07T12:00:00.000Z",
        "year": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Statistics action reference](actions/get-statistics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platerecognizer/latest/actions/get-statistics).

## Create Camera Monitoring Log

Creates a camera monitoring log in Plate Recognizer VisionAlert.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/create-camera-monitoring-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cameraId": "string",
  "upload": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/create-camera-monitoring-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cameraId": "string",
    "upload": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Camera Monitoring Log action reference](actions/create-camera-monitoring-log.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platerecognizer/latest/actions/create-camera-monitoring-log).
