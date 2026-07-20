# Printify: List Uploads

Retrieves uploads from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-uploads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-uploads?${params}`, {
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
| `limit` | number | no | Maximum number of uploads to return. |
| `page` | number | no | Result page to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "fileName": "Ava Chen",
          "id": "string",
          "mimeType": "string",
          "previewUrl": "https://example.com"
        }
      ],
      "perPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].fileName` | string |  |
| `data[].id` | string |  |
| `data[].mimeType` | string |  |
| `data[].previewUrl` | string |  |
| `perPage` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Printify API, this operation is `GET /uploads.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-uploads.md) for the provider-specific parameters and requirements.

