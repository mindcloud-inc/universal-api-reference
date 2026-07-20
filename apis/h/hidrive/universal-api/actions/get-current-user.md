# HiDrive: Get Current User

Retrieves the current user from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-current-user?${params}`, {
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
| `fields` | string | no | Comma-separated user fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "alias": "string",
      "email": "ava@example.com",
      "email_verified": true,
      "encrypted": true,
      "folder": {},
      "home": "string",
      "home_id": "string",
      "is_admin": true,
      "is_owner": true,
      "language": "string",
      "protocols": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | HiDrive account identifier. |
| `alias` | string | User alias. |
| `email` | string | User email address. |
| `email_verified` | boolean | Whether the email is verified. |
| `encrypted` | boolean | Whether the account uses encryption. |
| `folder` | object | Folder metadata. |
| `home` | string | User home path. |
| `home_id` | string | User home folder ID. |
| `is_admin` | boolean | Whether the user is an administrator. |
| `is_owner` | boolean | Whether the user is the owner. |
| `language` | string | User language setting. |
| `protocols` | object | Enabled protocol metadata. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /user/me` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

