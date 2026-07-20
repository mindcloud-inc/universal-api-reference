# Smartsheet: Delete Rows

Deletes rows from a Smartsheet sheet.

```
DELETE https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-rows?connectionId=$CONNECTION_ID&sheetId=1&ids=123%2C456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetId": "1",
  "ids": "123,456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-rows?${params}`, {
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
| `sheetId` | number | yes |  |
| `ids` | string | yes | Example: `123,456`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreRowsNotFound` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": [
        1
      ],
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
| `result[]` | number |  |
| `resultCode` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `DELETE /sheets/:sheetId/rows` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rows.md) for the provider-specific parameters and requirements.

