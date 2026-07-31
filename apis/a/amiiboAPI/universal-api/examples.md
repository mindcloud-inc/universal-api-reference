# Amiibo API Universal API Examples

These examples use the MindCloud API key and Amiibo API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Amiibo by ID



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id?${params}`, {
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
      "amiibo": {
        "amiiboSeries": "string",
        "character": "string",
        "gameSeries": "string",
        "head": "string",
        "image": "string",
        "name": "Ava Chen",
        "release": {
          "au": "2026-05-07T12:00:00.000Z",
          "eu": "2026-05-07T12:00:00.000Z",
          "jp": "2026-05-07T12:00:00.000Z",
          "na": "2026-05-07T12:00:00.000Z"
        },
        "tail": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Amiibo by ID action reference](actions/get-amiibo-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amiiboAPI/latest/actions/get-amiibo-by-id).
