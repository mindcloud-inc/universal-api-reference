# Seafile: List Libraries

Retrieves libraries from Seafile, optionally filtered by name.

```
GET https://connect.mindcloud.co/v1/universal/seafile/latest/actions/list-libraries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seafile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/list-libraries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/list-libraries?${params}`, {
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
      "encrypted": true,
      "head_commit_id": "string",
      "id": "string",
      "modifier_contact_email": "ava@example.com",
      "modifier_email": "ava@example.com",
      "modifier_name": "Ava Chen",
      "mtime": 1,
      "mtime_relative": "string",
      "name": "Ava Chen",
      "owner": "string",
      "owner_contact_email": "ava@example.com",
      "owner_name": "Ava Chen",
      "permission": "string",
      "root": "string",
      "salt": "string",
      "size": 1,
      "size_formatted": "string",
      "type": "string",
      "version": 1,
      "virtual": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `encrypted` | boolean |  |
| `head_commit_id` | string |  |
| `id` | string |  |
| `modifier_contact_email` | string |  |
| `modifier_email` | string |  |
| `modifier_name` | string |  |
| `mtime` | number |  |
| `mtime_relative` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `owner_contact_email` | string |  |
| `owner_name` | string |  |
| `permission` | string |  |
| `root` | string |  |
| `salt` | string |  |
| `size` | number |  |
| `size_formatted` | string |  |
| `type` | string |  |
| `version` | number |  |
| `virtual` | boolean |  |

## Native endpoint

Through the native Seafile API, this operation is `GET https://plus.seafile.com/api2/repos/` (base URL `https://plus.seafile.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-libraries.md) for the provider-specific parameters and requirements.

