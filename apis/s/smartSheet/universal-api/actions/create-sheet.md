# Smartsheet: Create Sheet

Creates a new sheet in Smartsheet.

```
POST https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-sheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/create-sheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns[]` | array<object> | no |  |
| `fromId` | number | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": {
        "accessLevel": "string",
        "columns": [
          {
            "id": 1,
            "index": 1,
            "primary": true,
            "title": "string",
            "type": "string",
            "validation": true,
            "version": 1,
            "width": 1
          }
        ],
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
| `result.columns[].id` | number |  |
| `result.columns[].index` | number |  |
| `result.columns[].primary` | boolean |  |
| `result.columns[].title` | string |  |
| `result.columns[].type` | string |  |
| `result.columns[].validation` | boolean |  |
| `result.columns[].version` | number |  |
| `result.columns[].width` | number |  |
| `result.id` | number |  |
| `result.name` | string |  |
| `result.permalink` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `POST /sheets` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sheet.md) for the provider-specific parameters and requirements.

