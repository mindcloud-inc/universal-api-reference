# Aspire: List Equipment Reading Logs

Retrieves equipment reading logs from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-reading-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-reading-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-equipment-reading-logs?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BranchID": 1,
      "BranchName": "Ava Chen",
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "DivisionID": 1,
      "DivisionName": "Ava Chen",
      "EquipmentID": 1,
      "EquipmentReadingLogID": 1,
      "LastModifiedByUserID": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "LogDate": "2026-05-07T12:00:00.000Z",
      "MeterReading": 1,
      "ReadingDate": "2026-05-07T12:00:00.000Z",
      "RouteID": 1,
      "RouteName": "Ava Chen",
      "TroubleCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BranchID` | number |  |
| `BranchName` | string |  |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `DivisionID` | number |  |
| `DivisionName` | string |  |
| `EquipmentID` | number |  |
| `EquipmentReadingLogID` | number |  |
| `LastModifiedByUserID` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |
| `LogDate` | date |  |
| `MeterReading` | number |  |
| `ReadingDate` | date |  |
| `RouteID` | number |  |
| `RouteName` | string |  |
| `TroubleCode` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET EquipmentReadingLogs` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipment-reading-logs.md) for the provider-specific parameters and requirements.

