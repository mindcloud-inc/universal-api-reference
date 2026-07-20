# SimFin Universal API Examples

These examples use the MindCloud API key and SimFin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download markets dataset

Retrieves the markets dataset from SimFin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-markets-dataset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-markets-dataset?${params}`, {
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
      "dataset": "string",
      "downloaded": true
    }
  ],
  "meta": {}
}
```

See the full [Download markets dataset action reference](actions/download-markets-dataset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simFin/latest/actions/download-markets-dataset).
