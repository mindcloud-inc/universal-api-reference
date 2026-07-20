# Aspire: Update Equipment Reading Log

Updates an existing equipment reading log in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-equipment-reading-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-equipment-reading-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logDate": "2026-05-07T12:00:00.000Z",
  "readingDate": "2026-05-07T12:00:00.000Z",
  "meterReading": 1,
  "equipmentReadingLogId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-equipment-reading-log', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logDate": "2026-05-07T12:00:00.000Z",
    "readingDate": "2026-05-07T12:00:00.000Z",
    "meterReading": 1,
    "equipmentReadingLogId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `equipmentId` | number | no |  |
| `logDate` | date | yes |  |
| `readingDate` | date | yes |  |
| `meterReading` | number | yes |  |
| `troubleCode` | string | no |  |
| `equipmentReadingLogId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT EquipmentReadingLogs` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-equipment-reading-log.md) for the provider-specific parameters and requirements.

