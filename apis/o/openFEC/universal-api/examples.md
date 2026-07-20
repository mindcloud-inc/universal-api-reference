# OpenFEC Universal API Examples

These examples use the MindCloud API key and OpenFEC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Candidates

Retrieves a list of candidates from OpenFEC.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidates?${params}`, {
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
      "active_through": 1,
      "candidate_id": "string",
      "cycles": [
        1
      ],
      "district": "string",
      "election_years": [
        1
      ],
      "incumbent_challenge_full": "string",
      "name": "Ava Chen",
      "office": "string",
      "office_full": "string",
      "party": "string",
      "party_full": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Candidates action reference](actions/list-candidates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openFEC/latest/actions/list-candidates).
