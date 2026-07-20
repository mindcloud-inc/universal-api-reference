# WhyDonate Universal API Examples

These examples use the MindCloud API key and WhyDonate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Widget Styles



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-widget-styles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-widget-styles?${params}`, {
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
      "data": {
        "styles": [
          {}
        ]
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [List Widget Styles action reference](actions/list-widget-styles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whyDonate/latest/actions/list-widget-styles).
