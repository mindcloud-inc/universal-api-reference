# Docusnap365 Universal API Examples

These examples use the MindCloud API key and Docusnap365 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/list-sites?${params}`, {
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
      "buildings": [
        {}
      ],
      "desc": "string",
      "iconId": "string",
      "id": "string",
      "isOpen": true,
      "label": "string",
      "realm": "string",
      "resourceTypeId": "string",
      "search": true,
      "segment": "string",
      "show": true,
      "userDefined": true
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docusnap365/latest/actions/list-sites).
