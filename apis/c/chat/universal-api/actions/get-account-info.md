# 2Chat: Get Account Info

Retrieves your account details from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info?${params}`, {
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
      "account": {
        "blocked": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "expiresAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "onTrial": true,
        "uuid": "string"
      },
      "limits": {
        "requestsPerMinute": 1
      },
      "success": true,
      "usage": {
        "apiRequestsAvailable": 1,
        "apiRequestsPlanDefault": 1,
        "numberCheckRequestsAvailable": 1,
        "numberCheckRequestsPlanDefault": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.blocked` | boolean |  |
| `account.createdAt` | date |  |
| `account.expiresAt` | date |  |
| `account.name` | string |  |
| `account.onTrial` | boolean |  |
| `account.uuid` | string |  |
| `limits.requestsPerMinute` | number |  |
| `success` | boolean |  |
| `usage.apiRequestsAvailable` | number |  |
| `usage.apiRequestsPlanDefault` | number |  |
| `usage.numberCheckRequestsAvailable` | number |  |
| `usage.numberCheckRequestsPlanDefault` | number |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /info` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

