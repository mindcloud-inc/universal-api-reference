# Veterans Affairs Facilities Universal API Examples

These examples use the MindCloud API key and Veterans Affairs Facilities connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Facility IDs

Retrieves VA facility IDs by facility type.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Facility IDs action reference](actions/list-facility-ids.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veteransAffairsFacilities/latest/actions/list-facility-ids).
