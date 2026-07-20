# ERPLY Books: Authenticate

Authenticates an ERPLY Books connection and returns session details.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/authenticate?${params}`, {
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
      "records": [
        {
          "berlinPOSAssetsURL": "https://example.com",
          "berlinPOSVersion": "string",
          "employeeID": "string",
          "employeeName": "Ava Chen",
          "epsiDownloadURLs": [
            {
              "operatingSystem": "https://example.com",
              "url": "https://example.com"
            }
          ],
          "epsiURL": "https://example.com",
          "groupID": "string",
          "groupName": "Ava Chen",
          "identityToken": "string",
          "ipAddress": "string",
          "isPasswordExpired": true,
          "loginUrl": "https://example.com",
          "remindUserToUpdateUsername": 1,
          "sessionKey": "string",
          "sessionLength": 1,
          "token": "string",
          "userID": "string",
          "userName": "Ava Chen"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].berlinPOSAssetsURL` | string |  |
| `records[].berlinPOSVersion` | string |  |
| `records[].employeeID` | string |  |
| `records[].employeeName` | string |  |
| `records[].epsiDownloadURLs[].operatingSystem` | string |  |
| `records[].epsiDownloadURLs[].url` | string |  |
| `records[].epsiURL` | string |  |
| `records[].groupID` | string |  |
| `records[].groupName` | string |  |
| `records[].identityToken` | string |  |
| `records[].ipAddress` | string |  |
| `records[].isPasswordExpired` | boolean |  |
| `records[].loginUrl` | string |  |
| `records[].remindUserToUpdateUsername` | number |  |
| `records[].sessionKey` | string |  |
| `records[].sessionLength` | number |  |
| `records[].token` | string |  |
| `records[].userID` | string |  |
| `records[].userName` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

