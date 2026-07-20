# Dropbox: Get Current Account

Retrieves the current account details from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-current-account?${params}`, {
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
      "accountId": "string",
      "accountType": {
        "tag": "string"
      },
      "country": "string",
      "disabled": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "isPaired": true,
      "locale": "string",
      "name": {
        "abbreviatedName": "Ava Chen",
        "displayName": "Ava Chen",
        "familiarName": "Ava Chen",
        "givenName": "Ava Chen",
        "surname": "Ava Chen"
      },
      "referralLink": "https://example.com",
      "rootInfo": {
        "homeNamespaceId": "Ava Chen",
        "rootNamespaceId": "Ava Chen",
        "tag": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountType.tag` | string |  |
| `country` | string |  |
| `disabled` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `isPaired` | boolean |  |
| `locale` | string |  |
| `name.abbreviatedName` | string |  |
| `name.displayName` | string |  |
| `name.familiarName` | string |  |
| `name.givenName` | string |  |
| `name.surname` | string |  |
| `referralLink` | string |  |
| `rootInfo.homeNamespaceId` | string |  |
| `rootInfo.rootNamespaceId` | string |  |
| `rootInfo.tag` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /users/get_current_account` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

