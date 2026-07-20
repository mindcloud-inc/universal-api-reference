# Umbler Talk: Get Current Member

Retrieves the current member profile from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member?${params}`, {
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
      "_t": "string",
      "cellphone": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "id": "string",
      "organizations": [
        {}
      ],
      "profilePictureUrl": "https://example.com",
      "signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `cellphone` | string |  |
| `createdAtUTC` | date |  |
| `displayName` | string |  |
| `emailAddress` | string |  |
| `id` | string |  |
| `organizations` | array<object> |  |
| `profilePictureUrl` | string |  |
| `signature` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/members/me/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-member.md) for the provider-specific parameters and requirements.

