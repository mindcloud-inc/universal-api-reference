# Nexiopay: Who am I



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i?${params}`, {
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
      "accessRights": {},
      "accountId": "string",
      "accountType": "string",
      "businessLegalName": "Ava Chen",
      "cognitoSub": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateLastModified": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "firstName": "Ava",
      "isApiUser": true,
      "lastName": "Chen",
      "payoutAccessRights": {},
      "phone": "string",
      "userName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessRights` | object |  |
| `accountId` | string |  |
| `accountType` | string |  |
| `businessLegalName` | string |  |
| `cognitoSub` | string |  |
| `dateCreated` | date |  |
| `dateLastModified` | date |  |
| `enabled` | boolean |  |
| `firstName` | string |  |
| `isApiUser` | boolean |  |
| `lastName` | string |  |
| `payoutAccessRights` | object |  |
| `phone` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /user/v3/account/whoAmI` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/who-am-i.md) for the provider-specific parameters and requirements.

