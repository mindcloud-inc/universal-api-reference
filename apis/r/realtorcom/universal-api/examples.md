# Realtor.com Universal API Examples

These examples use the MindCloud API key and Realtor.com connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Properties



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties?${params}`, {
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
      "@odata": {
        "context": "string",
        "count": 1,
        "nextLink": "https://example.com"
      },
      "value": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Properties action reference](actions/list-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realtorcom/latest/actions/list-properties).
