# Zoho Sign: List Folders

Retrieves folders from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-folders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "folders": [
        {
          "folderId": "string",
          "folderName": "Ava Chen"
        }
      ],
      "message": "string",
      "pageContext": {
        "hasMoreRows": true,
        "rowCount": 1,
        "sortColumn": "string",
        "sortOrder": "string",
        "startIndex": 1,
        "totalCount": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `folders` | array<object> |  |
| `folders[].folderId` | string |  |
| `folders[].folderName` | string |  |
| `message` | string |  |
| `pageContext` | object |  |
| `pageContext.hasMoreRows` | boolean |  |
| `pageContext.rowCount` | number |  |
| `pageContext.sortColumn` | string |  |
| `pageContext.sortOrder` | string |  |
| `pageContext.startIndex` | number |  |
| `pageContext.totalCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /folders` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

