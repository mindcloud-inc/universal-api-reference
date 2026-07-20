# Podio: Get User Status

Retrieves user status details from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status?${params}`, {
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
      "betas": [
        "string"
      ],
      "calendarCode": "string",
      "flags": [
        "string"
      ],
      "inbox": {},
      "inboxNew": 1,
      "mailbox": {},
      "messageUnreadCount": 1,
      "presence": {},
      "profile": {},
      "properties": {},
      "push": {},
      "referral": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `betas` | array<string> |  |
| `calendarCode` | string |  |
| `flags` | array<string> |  |
| `inbox` | object |  |
| `inboxNew` | number |  |
| `mailbox` | object |  |
| `messageUnreadCount` | number |  |
| `presence` | object |  |
| `profile` | object |  |
| `properties` | object |  |
| `push` | object |  |
| `referral` | object |  |
| `user` | object |  |

## Native endpoint

Through the native Podio API, this operation is `GET /user/status` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-status.md) for the provider-specific parameters and requirements.

