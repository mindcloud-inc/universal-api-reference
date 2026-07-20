# Ugosign: List Members

Retrieves members from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-members?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerifiedAt": "2026-05-07T12:00:00.000Z",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "job": "string",
      "locale": "string",
      "onboarded": true,
      "phoneNumber": "string",
      "position": "string",
      "role": "string",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `emailVerifiedAt` | date |  |
| `familyName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `job` | string |  |
| `locale` | string |  |
| `onboarded` | boolean |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `role` | string |  |
| `slug` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ugosign API, this operation is `GET /v1/members` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

