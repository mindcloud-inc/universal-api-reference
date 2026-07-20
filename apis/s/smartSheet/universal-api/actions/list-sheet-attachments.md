# Smartsheet: List Sheet Attachments

Retrieves attachments from a Smartsheet sheet.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheet-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheet-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0&sheetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sheetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheet-attachments?${params}`, {
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
| `includeAll` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNumber": 1,
      "pageSize": 1,
      "totalCount": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /sheets/:sheetId/attachments` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sheet-attachments.md) for the provider-specific parameters and requirements.

