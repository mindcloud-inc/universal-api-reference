# LastPass: Get User Data

Retrieves user data from LastPass.

```
GET https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LastPass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-user-data?${params}`, {
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
      "admin": true,
      "applications": 1,
      "attachments": 1,
      "count": 1,
      "created": "string",
      "disabled": true,
      "duousername": "Ava Chen",
      "formfills": 1,
      "fullname": "Ava Chen",
      "groups": [
        {}
      ],
      "hasSharingKeys": true,
      "lastLogin": "string",
      "lastPwChange": "string",
      "legacytotalscore": "string",
      "mpstrength": "string",
      "neverloggedin": true,
      "notes": 1,
      "passwordResetRequired": true,
      "sites": 1,
      "total": 1,
      "totalscore": "string",
      "userId": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean | Whether the user is an admin. |
| `applications` | number | Number of applications for the user. |
| `attachments` | number | Number of attachments for the user. |
| `count` | number | Number of users included in this response. |
| `created` | string | When the user was created in LastPass. |
| `disabled` | boolean | Whether the user is disabled. |
| `duousername` | string | Associated Duo username, when present. |
| `formfills` | number | Number of form fills for the user. |
| `fullname` | string | User full name in LastPass. |
| `groups` | array<object> | Groups assigned to the user. |
| `hasSharingKeys` | boolean | Whether the user has sharing keys. |
| `lastLogin` | string | When the user last logged in. |
| `lastPwChange` | string | When the user last changed their password. |
| `legacytotalscore` | string | Legacy LastPass total security score for the user. |
| `mpstrength` | string | Reported LastPass master password strength score. |
| `neverloggedin` | boolean | Whether the user has never logged in. |
| `notes` | number | Number of secure notes for the user. |
| `passwordResetRequired` | boolean | Whether a password reset is required. |
| `sites` | number | Number of sites for the user. |
| `total` | number | Total number of users returned by LastPass. |
| `totalscore` | string | LastPass total security score for the user. |
| `userId` | string | LastPass user ID. |
| `username` | string | LastPass username or email address. |

## Native endpoint

Through the native LastPass API, this operation is `POST /enterpriseapi.php` (base URL `https://lastpass.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data.md) for the provider-specific parameters and requirements.

