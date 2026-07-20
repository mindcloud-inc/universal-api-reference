# ScreenshotOne Universal API Examples

These examples use the MindCloud API key and ScreenshotOne connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/get-usage?${params}`, {
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
      "available": 1,
      "concurrency": {
        "limit": 1,
        "remaining": 1,
        "reset": 1
      },
      "total": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenshotOne/latest/actions/get-usage).
