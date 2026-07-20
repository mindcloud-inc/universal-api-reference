# BCDR Cloud Universal API Examples

These examples use the MindCloud API key and BCDR Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Portal Server



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCDRCloudAPI/latest/actions/get-portal-server?${params}`, {
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
      "item0": "string",
      "item1": "string",
      "item2": "string",
      "item3": 1,
      "item4": 1,
      "item5": 1,
      "item6": 1,
      "item7": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Portal Server action reference](actions/get-portal-server.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bCDRCloudAPI/latest/actions/get-portal-server).
