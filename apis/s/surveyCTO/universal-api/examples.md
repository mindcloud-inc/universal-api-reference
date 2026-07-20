# SurveyCTO Universal API Examples

These examples use the MindCloud API key and SurveyCTO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Datasets

Retrieves all available datasets from SurveyCTO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyCTO/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyCTO/latest/actions/list-datasets?${params}`, {
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

See the full [List Datasets action reference](actions/list-datasets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/surveyCTO/latest/actions/list-datasets).
