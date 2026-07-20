# Nanonets OCR: List Workflows



```
GET https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-workflows?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "fields": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "id": "string",
      "settings": {
        "tableCapture": true
      },
      "tableHeaders": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `createdAt` | string |  |
| `description` | string |  |
| `fields[].id` | string |  |
| `fields[].name` | string |  |
| `id` | string |  |
| `settings.tableCapture` | boolean |  |
| `tableHeaders[].id` | string |  |
| `tableHeaders[].name` | string |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `GET /workflows` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

