# Agicap Universal API Examples

These examples use the MindCloud API key and Agicap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bank Journal Export Details

Retrieves details for a bank journal export from Agicap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agicap/latest/actions/get-bank-journal-export-details?connectionId=$CONNECTION_ID&entityId=140010&exportId=47a62f3d-6885-4f33-a7d2-40a4470b3a5f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "140010",
  "exportId": "47a62f3d-6885-4f33-a7d2-40a4470b3a5f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agicap/latest/actions/get-bank-journal-export-details?${params}`, {
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
      "bankJournalExportIndexInYear": 1,
      "entityName": "Ava Chen",
      "entries": [
        {}
      ],
      "exportId": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Bank Journal Export Details action reference](actions/get-bank-journal-export-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agicap/latest/actions/get-bank-journal-export-details).

## Create Bank Journal Export

Creates a bank journal export in Agicap for ready-to-export entries.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agicap/latest/actions/create-bank-journal-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "140010",
  "exportId": "47a62f3d-6885-4f33-a7d2-40a4470b3a5f"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agicap/latest/actions/create-bank-journal-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "140010",
    "exportId": "47a62f3d-6885-4f33-a7d2-40a4470b3a5f"
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
      "bankJournalExportIndexInYear": 1,
      "entityName": "Ava Chen",
      "entries": [
        {}
      ],
      "exportId": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bank Journal Export action reference](actions/create-bank-journal-export.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agicap/latest/actions/create-bank-journal-export).
