# Smartsheet: Copy Rows

Copies rows to another sheet in Smartsheet.

```
POST https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/copy-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/copy-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sheetId": 1,
  "rowIds[]": [
    1
  ],
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/copy-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sheetId": 1,
    "rowIds[]": [1],
    "to": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sheetId` | number | yes |  |
| `rowIds[]` | array<number> | yes |  |
| `to` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |
| `ignoreRowsNotFound` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destinationSheetId": 1,
      "rowMappings": [
        {
          "from": 1,
          "to": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinationSheetId` | number |  |
| `rowMappings[].from` | number |  |
| `rowMappings[].to` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `POST /sheets/:sheetId/rows/copy` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-rows.md) for the provider-specific parameters and requirements.

