# Revel Digital: List Media



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-media?${params}`, {
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
      "advertiser_id": "string",
      "end_date": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "file_url": "https://example.com",
      "group_id": "string",
      "group_name": "Ava Chen",
      "height": 1,
      "id": "string",
      "is_shared": true,
      "mime_type": "string",
      "name": "Ava Chen",
      "sha_512": "string",
      "start_date": "string",
      "tags": "string",
      "thumbnail_url": "https://example.com",
      "uploaded_by_id": "string",
      "uploaded_on": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiser_id` | string |  |
| `end_date` | string |  |
| `file_name` | string |  |
| `file_size` | number |  |
| `file_url` | string |  |
| `group_id` | string |  |
| `group_name` | string |  |
| `height` | number |  |
| `id` | string |  |
| `is_shared` | boolean |  |
| `mime_type` | string |  |
| `name` | string |  |
| `sha_512` | string |  |
| `start_date` | string |  |
| `tags` | string |  |
| `thumbnail_url` | string |  |
| `uploaded_by_id` | string |  |
| `uploaded_on` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /media` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

