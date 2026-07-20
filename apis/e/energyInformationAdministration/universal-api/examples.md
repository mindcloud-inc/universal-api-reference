# Energy Information Administration Universal API Examples

These examples use the MindCloud API key and Energy Information Administration connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Total Energy Data

Retrieves total energy data from EIA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-total-energy-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-total-energy-data?${params}`, {
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

See the full [Query Total Energy Data action reference](actions/query-total-energy-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/energyInformationAdministration/latest/actions/query-total-energy-data).
