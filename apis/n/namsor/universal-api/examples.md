# Namsor Universal API Examples

These examples use the MindCloud API key and Namsor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Api Status

Retrieves the current Namsor API status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/api-status?${params}`, {
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
      "classifiers": [
        {}
      ],
      "softwareVersion": {}
    }
  ],
  "meta": {}
}
```

See the full [Api Status action reference](actions/api-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/namsor/latest/actions/api-status).
