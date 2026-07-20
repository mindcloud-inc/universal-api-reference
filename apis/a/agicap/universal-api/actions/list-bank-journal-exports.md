# Agicap: List Bank Journal Exports

Retrieves previous bank journal exports from Agicap.

```
GET https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-bank-journal-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agicap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-bank-journal-exports?connectionId=$CONNECTION_ID&entityId=140010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "140010"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-bank-journal-exports?${params}`, {
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
| `size` | number | no | Number of exports to return. Agicap documents a maximum of 100. Default: `100`. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | date | no | Return exports after this ISO 8601 date cursor or filter value. Example: `2026-01-01T00:00:00Z`. |
| `before` | date | no | Return exports before this ISO 8601 date cursor or filter value. Example: `2026-12-31T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exportDateUtc": "2026-05-07T12:00:00.000Z",
      "exportId": "string",
      "exportIndexInYear": 1,
      "exportYear": 1,
      "indexInYearOfFirstEntryInBankJournal": 1,
      "indexInYearOfLastEntryInBankJournal": 1,
      "numberOfEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exportDateUtc` | date | Export date-time in UTC. |
| `exportId` | string | Unique ID of the bank journal export. |
| `exportIndexInYear` | number | Index of the bank journal export in the export year. |
| `exportYear` | number | Year the export was done. |
| `indexInYearOfFirstEntryInBankJournal` | number | Index in export year of the first entry in this bank journal export. |
| `indexInYearOfLastEntryInBankJournal` | number | Index in export year of the last entry in this bank journal export. |
| `numberOfEntries` | number | Number of entries in the bank journal export. |

## Native endpoint

Through the native Agicap API, this operation is `GET /public/treasury-bank-journal/v1/entities/:entityId/exports` (base URL `https://api.agicap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bank-journal-exports.md) for the provider-specific parameters and requirements.

