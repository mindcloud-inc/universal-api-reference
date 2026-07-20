# Ubidots Universal API Examples

These examples use the MindCloud API key and Ubidots connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all Devices



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-devices?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isActive": true,
      "label": "string",
      "name": "Ava Chen",
      "organization": {},
      "properties": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com",
      "variables": "string",
      "variablesNumber": 1
    }
  ],
  "meta": {}
}
```

See the full [Get all Devices action reference](actions/get-all-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ubidots/latest/actions/get-all-devices).
