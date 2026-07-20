# Fabric: Get My Profile

Retrieves your profile from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-my-profile?${params}`, {
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
      "createdAt": "string",
      "email": "ava@example.com",
      "emailIngestionAddress": "ava@example.com",
      "groups": [
        {}
      ],
      "id": "string",
      "modifiedAt": "string",
      "name": "Ava Chen",
      "onboarding": {},
      "pictureUrlCdn": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `email` | string |  |
| `emailIngestionAddress` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `onboarding` | object |  |
| `pictureUrlCdn` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/users/me` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

