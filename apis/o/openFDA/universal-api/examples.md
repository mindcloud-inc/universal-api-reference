# OpenFDA Universal API Examples

These examples use the MindCloud API key and OpenFDA connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Animal Veterinary Event Records

Counts animal veterinary event records in OpenFDA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/count-animal-veterinary-event-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/count-animal-veterinary-event-records?${params}`, {
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
      "meta": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Count Animal Veterinary Event Records action reference](actions/count-animal-veterinary-event-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openFDA/latest/actions/count-animal-veterinary-event-records).
