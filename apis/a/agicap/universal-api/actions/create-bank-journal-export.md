# Agicap: Create Bank Journal Export

Creates a bank journal export in Agicap for ready-to-export entries.

```
POST https://connect.mindcloud.co/v1/universal/agicap/latest/actions/create-bank-journal-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agicap `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | Agicap entity identifier. Example: `140010`. |
| `exportId` | string | yes | Caller-generated UUID for the export. Example: `47a62f3d-6885-4f33-a7d2-40a4470b3a5f`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentExportCounts.currentBankJournalsCountInYear` | number | no | Optional number of bank journals already created this year outside Agicap, for first export numbering continuity. Example: `0`. |
| `currentExportCounts.currentBankJournalEntriesCountInYear` | number | no | Optional number of bank journal entries already created this year outside Agicap, for first export numbering continuity. Example: `0`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankJournalExportIndexInYear` | number | Index of the bank journal export in the current year. |
| `entityName` | string | Name of the entity. |
| `entries` | array<object> | Bank journal entries included in the export when the API returns a 200 response. |
| `exportId` | string | Identifier of the export. |
| `year` | number | UTC year when the bank journal was exported. |

## Native endpoint

Through the native Agicap API, this operation is `POST /public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId` (base URL `https://api.agicap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bank-journal-export.md) for the provider-specific parameters and requirements.

