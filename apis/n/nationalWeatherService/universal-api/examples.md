# National Weather Service Universal API Examples

These examples use the MindCloud API key and National Weather Service connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Alert Types

Retrieves alert types from National Weather Service.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-alert-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-alert-types?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Alert Types action reference](actions/list-alert-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nationalWeatherService/latest/actions/list-alert-types).
