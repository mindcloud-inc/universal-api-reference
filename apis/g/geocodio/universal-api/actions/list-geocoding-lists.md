# Geocodio: List Geocoding Lists

Retrieves geocoding lists from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-geocoding-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-geocoding-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-geocoding-lists?${params}`, {
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
      "currentPage": 1,
      "data": [
        {
          "downloadUrl": "https://example.com",
          "expiresAt": "2026-05-07T12:00:00.000Z",
          "fields": [
            "string"
          ],
          "file": {
            "estimatedRowsCount": 1,
            "filename": "Ava Chen"
          },
          "id": 1,
          "status": {
            "message": "string",
            "progress": 1,
            "state": "string",
            "timeLeftDescription": "string",
            "timeLeftSeconds": 1
          }
        }
      ],
      "firstPageUrl": "https://example.com",
      "from": 1,
      "nextPageUrl": "https://example.com",
      "path": "https://example.com",
      "perPage": 1,
      "prevPageUrl": "https://example.com",
      "to": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number | Current page number. |
| `data` | array<object> | Uploaded geocoding lists. |
| `data[].downloadUrl` | string | Download URL when available. |
| `data[].expiresAt` | date | Result expiration time. |
| `data[].fields` | array<string> | Requested data append fields. |
| `data[].file.estimatedRowsCount` | number | Estimated number of rows. |
| `data[].file.filename` | string | Uploaded filename. |
| `data[].id` | number | List ID. |
| `data[].status.message` | string | Status message. |
| `data[].status.progress` | number | Processing progress percentage. |
| `data[].status.state` | string | Processing state. |
| `data[].status.timeLeftDescription` | string | Estimated time remaining. |
| `data[].status.timeLeftSeconds` | number | Estimated seconds remaining. |
| `firstPageUrl` | string | First page URL. |
| `from` | number | First item index on the page. |
| `nextPageUrl` | string | Next page URL. |
| `path` | string | Pagination path. |
| `perPage` | number | Rows per page. |
| `prevPageUrl` | string | Previous page URL. |
| `to` | number | Last item index on the page. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /lists` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-geocoding-lists.md) for the provider-specific parameters and requirements.

