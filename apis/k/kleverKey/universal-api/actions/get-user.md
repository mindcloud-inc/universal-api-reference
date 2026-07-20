# KleverKey: Get User



```
GET https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-user?connectionId=$CONNECTION_ID&organizationId=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID |
| `userId` | number | yes | User ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessGroups": [
        {}
      ],
      "cultureCode": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "organizationIds": [
        1
      ],
      "roles": [
        {}
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessGroups` | array<object> |  |
| `cultureCode` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `organizationIds` | array<number> |  |
| `roles` | array<object> |  |
| `type` | number |  |

## Native endpoint

Through the native KleverKey API, this operation is `GET /api/v1/organizations/:organizationId/users/:userId` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

