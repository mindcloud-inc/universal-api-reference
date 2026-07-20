# bitFit Asset Management Software Universal API Examples

These examples use the MindCloud API key and bitFit Asset Management Software connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitFitAssetManagementSoftware/latest/actions/list-assets?${params}`, {
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Assets action reference](actions/list-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitFitAssetManagementSoftware/latest/actions/list-assets).
