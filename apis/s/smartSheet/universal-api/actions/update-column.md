# Smartsheet: Update Column

Updates an existing column in a Smartsheet sheet.

```
PUT https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "columnId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/update-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "columnId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `columnId` | number | yes |  |
| `title` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no |  |
| `options[]` | array<string> | no |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "id": 1,
        "index": 1,
        "options": [
          "string"
        ],
        "title": "string",
        "type": "string",
        "validation": true,
        "width": 1
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
| `result.id` | number |  |
| `result.index` | number |  |
| `result.options[]` | string |  |
| `result.title` | string |  |
| `result.type` | string |  |
| `result.validation` | boolean |  |
| `result.width` | number |  |
| `resultCode` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `PUT /sheets/:sheetId/columns/:columnId` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-column.md) for the provider-specific parameters and requirements.

