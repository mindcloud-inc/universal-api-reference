# Dropbox: Get Account

Retrieves an account's details from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-account?connectionId=$CONNECTION_ID&accountId=dbid%3AAADkOwgZqe2Om-IPCSww7iqedziBN30UYRw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "dbid:AADkOwgZqe2Om-IPCSww7iqedziBN30UYRw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-account?${params}`, {
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
| `accountId` | string | yes | The account ID to look up. Example: `dbid:AADkOwgZqe2Om-IPCSww7iqedziBN30UYRw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "disabled": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "isTeammate": true,
      "name": {
        "abbreviatedName": "Ava Chen",
        "displayName": "Ava Chen",
        "familiarName": "Ava Chen",
        "givenName": "Ava Chen",
        "surname": "Ava Chen"
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
| `disabled` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `isTeammate` | boolean |  |
| `name.abbreviatedName` | string |  |
| `name.displayName` | string |  |
| `name.familiarName` | string |  |
| `name.givenName` | string |  |
| `name.surname` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /users/get_account` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

