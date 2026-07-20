# Wufoo: List Users

Retrieves users from Wufoo.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-users?${params}`, {
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
      "adminAccess": "string",
      "company": "string",
      "createForms": "string",
      "createReports": "string",
      "createThemes": "string",
      "email": "ava@example.com",
      "hash": "string",
      "httpsEnabled": "string",
      "image": "string",
      "imageUrlBig": "https://example.com",
      "imageUrlSmall": "https://example.com",
      "isAccountOwner": "string",
      "linkForms": "https://example.com",
      "linkReports": "https://example.com",
      "timeZone": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminAccess` | string | Whether the user has admin access. |
| `company` | string | Company name on the Wufoo account. |
| `createForms` | string | Whether the user can create forms. |
| `createReports` | string | Whether the user can create reports. |
| `createThemes` | string | Whether the user can create themes. |
| `email` | string | User email address. |
| `hash` | string | Wufoo user hash identifier. |
| `httpsEnabled` | string | Whether HTTPS is enabled for the account. |
| `image` | string | Wufoo avatar image name. |
| `imageUrlBig` | string | Large avatar image URL. |
| `imageUrlSmall` | string | Small avatar image URL. |
| `isAccountOwner` | string | Whether the user owns the account. |
| `linkForms` | string | API URL for the user's forms. |
| `linkReports` | string | API URL for the user's reports. |
| `timeZone` | string | User time zone offset. |
| `user` | string | Wufoo username. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /users.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

