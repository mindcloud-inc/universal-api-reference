# Agicap: Get Bank Journal Export Details

Retrieves details for a bank journal export from Agicap.

```
GET https://connect.mindcloud.co/v1/universal/agicap/latest/actions/get-bank-journal-export-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agicap `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | Agicap entity identifier. Example: `140010`. |
| `exportId` | string | yes | Unique export identifier returned by the export list action. Example: `47a62f3d-6885-4f33-a7d2-40a4470b3a5f`. |

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
| `entries` | array<object> | Bank journal entries included in the export. |
| `exportId` | string | Identifier of the export. |
| `year` | number | UTC year when the bank journal was exported. |

## Native endpoint

Through the native Agicap API, this operation is `GET /public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId` (base URL `https://api.agicap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bank-journal-export-details.md) for the provider-specific parameters and requirements.

