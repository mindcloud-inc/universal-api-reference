# Smartsheet: Move Sheet

Moves a sheet in Smartsheet.

```
PUT https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/move-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/move-sheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "destinationId": 1,
  "destinationType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/move-sheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "destinationId": 1,
    "destinationType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `destinationId` | number | yes |  |
| `destinationType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "accessLevel": "string",
        "id": 1,
        "name": "Ava Chen",
        "permalink": "https://example.com"
      },
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result.accessLevel` | string |  |
| `result.id` | number |  |
| `result.name` | string |  |
| `result.permalink` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `POST /sheets/:sheetId/move` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-sheet.md) for the provider-specific parameters and requirements.

