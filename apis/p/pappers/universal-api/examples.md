# Pappers Universal API Examples

These examples use the MindCloud API key and Pappers connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Usage



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-api-usage?${params}`, {
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
      "jetonsAbonnement": 1,
      "jetonsAbonnementUtilises": 1,
      "jetonsPayAsYouGoRestants": 1
    }
  ],
  "meta": {}
}
```

See the full [Get API Usage action reference](actions/get-api-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pappers/latest/actions/get-api-usage).
