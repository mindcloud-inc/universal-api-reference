# PdfFiller: List Folders

Retrieves folders from PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-folders?${params}`, {
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
      "current_page": 1,
      "items": [
        {
          "documents_count": 1,
          "folder_id": 1,
          "folders_count": 1,
          "name": "Ava Chen",
          "parent_id": 1
        }
      ],
      "next_page_url": "https://example.com",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `items[].documents_count` | number |  |
| `items[].folder_id` | number |  |
| `items[].folders_count` | number |  |
| `items[].name` | string |  |
| `items[].parent_id` | number |  |
| `next_page_url` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/folders` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

