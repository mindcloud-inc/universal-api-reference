# Boost Universal API Examples

These examples use the MindCloud API key and Boost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Activity

Retrieves an activity type from Boost by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-activity?connectionId=$CONNECTION_ID&activityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-activity?${params}`, {
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
      "boostId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Activity action reference](actions/get-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boost/latest/actions/get-activity).
