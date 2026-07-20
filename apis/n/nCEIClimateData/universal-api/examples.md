# NCEI Climate Data Universal API Examples

These examples use the MindCloud API key and NCEI Climate Data connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Datasets

Finds climate datasets in NCEI Climate Data by filter criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/list-datasets?${params}`, {
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
      "datacoverage": 1,
      "id": "string",
      "maxdate": "2026-05-07T12:00:00.000Z",
      "mindate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Datasets action reference](actions/list-datasets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nCEIClimateData/latest/actions/list-datasets).
