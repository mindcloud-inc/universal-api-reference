# RightSignature: Get Me

Retrieves the authenticated RightSignature user profile.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me?${params}`, {
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
      "avatarUrl": "https://example.com",
      "cancellationDate": "string",
      "canSendDocuments": true,
      "company": "string",
      "email": "ava@example.com",
      "id": "string",
      "isGracePeriod": true,
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `cancellationDate` | string |  |
| `canSendDocuments` | boolean |  |
| `company` | string |  |
| `email` | string |  |
| `id` | string |  |
| `isGracePeriod` | boolean |  |
| `name` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /me` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-me.md) for the provider-specific parameters and requirements.

