# Chatwork: Get My Profile



```
GET https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile?${params}`, {
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
      "accountId": 1,
      "avatarImageUrl": "https://example.com",
      "chatworkId": "string",
      "department": "string",
      "facebook": "string",
      "introduction": "string",
      "loginMail": "string",
      "mail": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "roomId": 1,
      "skype": "string",
      "telExtension": "string",
      "telMobile": "string",
      "telOrganization": "string",
      "title": "string",
      "twitter": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `avatarImageUrl` | string |  |
| `chatworkId` | string |  |
| `department` | string |  |
| `facebook` | string |  |
| `introduction` | string |  |
| `loginMail` | string |  |
| `mail` | string |  |
| `name` | string |  |
| `organizationId` | number |  |
| `organizationName` | string |  |
| `roomId` | number |  |
| `skype` | string |  |
| `telExtension` | string |  |
| `telMobile` | string |  |
| `telOrganization` | string |  |
| `title` | string |  |
| `twitter` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Chatwork API, this operation is `GET /me` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

