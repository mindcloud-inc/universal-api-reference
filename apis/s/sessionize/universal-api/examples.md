# Sessionize Universal API Examples

These examples use the MindCloud API key and Sessionize connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Event Data

Retrieves all event data from Sessionize.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "jl4ktls0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data?${params}`, {
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
      "categories": [
        {}
      ],
      "questions": [
        {}
      ],
      "rooms": [
        {}
      ],
      "sessions": [
        {}
      ],
      "speakers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get All Event Data action reference](actions/get-all-event-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sessionize/latest/actions/get-all-event-data).
