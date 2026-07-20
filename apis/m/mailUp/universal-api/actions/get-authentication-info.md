# MailUp: Get Authentication Info

Retrieves authenticated user and console info from MailUp.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-authentication-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-authentication-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-authentication-info?${params}`, {
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
      "accountName": "Ava Chen",
      "company": "string",
      "expiryDate": "string",
      "isTrial": true,
      "uID": "string",
      "url": "https://example.com",
      "username": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `company` | string |  |
| `expiryDate` | string |  |
| `isTrial` | boolean |  |
| `uID` | string |  |
| `url` | string |  |
| `username` | string |  |
| `version` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/Authentication/Info` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authentication-info.md) for the provider-specific parameters and requirements.

