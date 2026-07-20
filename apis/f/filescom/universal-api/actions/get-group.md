# Files.com: Get Group

Finds a group in Files.com by ID.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-group?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-group?${params}`, {
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
| `id` | number | yes | Numeric group ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_ids": "string",
      "allowed_ips": "string",
      "dav_permission": true,
      "ftp_permission": true,
      "id": 1,
      "name": "Ava Chen",
      "restapi_permission": true,
      "sftp_permission": true,
      "user_ids": "string",
      "usernames": "Ava Chen",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin_ids` | string |  |
| `allowed_ips` | string |  |
| `dav_permission` | boolean |  |
| `ftp_permission` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `restapi_permission` | boolean |  |
| `sftp_permission` | boolean |  |
| `user_ids` | string |  |
| `usernames` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /groups/:id` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

