# Smartsheet: Get Sheet Summary

Retrieves a sheet summary from Smartsheet.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-sheet-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-sheet-summary?connectionId=$CONNECTION_ID&sheetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/get-sheet-summary?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |
| `exclude` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[]` | object | Sheet summary field returned by Smartsheet. |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /sheets/:sheetId/summary` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sheet-summary.md) for the provider-specific parameters and requirements.

