# PdfFiller: List Templates

Retrieves templates from PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates?${params}`, {
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
          "created": 1,
          "fillable": true,
          "folder": {
            "folder_id": 1,
            "name": "Ava Chen"
          },
          "id": 1,
          "name": "Ava Chen",
          "status": "string",
          "type": "string",
          "updated": 1
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
| `items[].created` | number |  |
| `items[].fillable` | boolean |  |
| `items[].folder.folder_id` | number |  |
| `items[].folder.name` | string |  |
| `items[].id` | number |  |
| `items[].name` | string |  |
| `items[].status` | string |  |
| `items[].type` | string |  |
| `items[].updated` | number |  |
| `next_page_url` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/templates` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

