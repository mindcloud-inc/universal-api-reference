# Smartsheet: List Sheets

Retrieves sheets from Smartsheet.

```
GET https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartsheet `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSheet/latest/actions/list-sheets?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Optional response elements to include in each sheet record. Example: `sheetVersion,source`. |
| `includeAll` | boolean | no |  |
| `modifiedSince` | date | no | Only return sheets modified on or after this date and time. |
| `numericDates` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "accessLevel": "string",
          "createdAt": "string",
          "id": 1,
          "modifiedAt": "string",
          "name": "Ava Chen",
          "permalink": "https://example.com"
        }
      ],
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
| `data[].accessLevel` | string |  |
| `data[].createdAt` | string |  |
| `data[].id` | number |  |
| `data[].modifiedAt` | string |  |
| `data[].name` | string |  |
| `data[].permalink` | string |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Smartsheet API, this operation is `GET /sheets` (base URL `https://api.smartsheet.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sheets.md) for the provider-specific parameters and requirements.

