# Files.com: Get Site

Retrieves current site settings from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "dav_enabled": true,
      "email": "ava@example.com",
      "ftp_enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "sftp_enabled": true,
      "sharing_enabled": true,
      "ssl_required": true,
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `dav_enabled` | boolean |  |
| `email` | string |  |
| `ftp_enabled` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `sftp_enabled` | boolean |  |
| `sharing_enabled` | boolean |  |
| `ssl_required` | boolean |  |
| `subdomain` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /site` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

