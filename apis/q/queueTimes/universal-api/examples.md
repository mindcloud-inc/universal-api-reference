# Queue Times Universal API Examples

These examples use the MindCloud API key and Queue Times connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Park Queue Times



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times?${params}`, {
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
      "lands": [
        {
          "id": 1,
          "name": "Ava Chen",
          "rides": [
            {
              "id": 1,
              "is_open": true,
              "last_updated": "string",
              "name": "Ava Chen",
              "wait_time": 1
            }
          ]
        }
      ],
      "rides": [
        {
          "id": 1,
          "is_open": true,
          "last_updated": "string",
          "name": "Ava Chen",
          "wait_time": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Park Queue Times action reference](actions/get-park-queue-times.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/queueTimes/latest/actions/get-park-queue-times).
