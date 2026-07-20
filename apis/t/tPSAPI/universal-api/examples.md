# TPS API Universal API Examples

These examples use the MindCloud API key and TPS API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Screen Phone Numbers

Screens phone numbers against TPS and CTPS lists in TPS API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers?connectionId=$CONNECTION_ID&phoneNumbers=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumbers": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers?${params}`, {
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

See the full [Screen Phone Numbers action reference](actions/screen-phone-numbers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tPSAPI/latest/actions/screen-phone-numbers).
