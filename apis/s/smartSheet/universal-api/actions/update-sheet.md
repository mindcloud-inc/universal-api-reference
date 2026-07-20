# Smartsheet: Update Sheet

Updates an existing sheet in Smartsheet.

```
PUT https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-sheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-sheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `name` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectSettings` | object | no |  |
| `userSettings` | object | no |  |

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
      "resultCode": 1,
      "version": 1
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
| `version` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `PUT /sheets/:sheetId` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sheet.md) for the provider-specific parameters and requirements.

