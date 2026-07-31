# HTTP Dogs Universal API Examples

These examples use the MindCloud API key and HTTP Dogs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get HTTP Status Dog AVIF



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-avif?connectionId=$CONNECTION_ID&statusCode=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusCode": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-avif?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get HTTP Status Dog AVIF action reference](actions/get-http-status-dog-avif.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTTPDogs/latest/actions/get-http-status-dog-avif).
