# MOBIDI Universal API Examples

These examples use the MindCloud API key and MOBIDI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Record Counts

Retrieves record counts for a MOBIDI query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-record-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-record-counts?${params}`, {
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

See the full [Query Record Counts action reference](actions/query-record-counts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mOBIDI/latest/actions/query-record-counts).

## Create Or Update Record

Creates or updates a record in MOBIDI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-or-update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entry": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-or-update-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entry": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "AlternateId": "string",
      "annotations": [
        {}
      ],
      "attachments": [
        {}
      ],
      "attributes": [
        {}
      ],
      "Info": "string",
      "IsReadonlyRecord": true,
      "points": {},
      "record": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Record action reference](actions/create-or-update-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mOBIDI/latest/actions/create-or-update-record).
