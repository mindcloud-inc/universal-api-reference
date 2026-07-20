# openFDA Drug Universal API Examples

These examples use the MindCloud API key and openFDA Drug connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Drug Adverse Event Records

Counts drug adverse event records in openFDA Drug by field.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records?connectionId=$CONNECTION_ID&count=patient.drug.medicinalproduct.exact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "patient.drug.medicinalproduct.exact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/count-drug-adverse-event-records?${params}`, {
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
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Count Drug Adverse Event Records action reference](actions/count-drug-adverse-event-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openFDADrug/latest/actions/count-drug-adverse-event-records).
