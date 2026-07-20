# Smartsheet: Delete Sheet

Deletes an existing sheet from Smartsheet.

```
DELETE https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-sheet?connectionId=$CONNECTION_ID&sheetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/delete-sheet?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
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
| `resultCode` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `DELETE /sheets/:sheetId` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sheet.md) for the provider-specific parameters and requirements.

