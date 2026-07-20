# Clockify: Get Member Profile

Retrieves a member profile from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-member-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-member-profile?connectionId=$CONNECTION_ID&workspaceId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-member-profile?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "hasPassword": true,
      "hasPendingApprovalRequest": true,
      "imageUrl": "https://example.com",
      "name": "Ava Chen",
      "userCustomFieldValues": [
        [
          "string"
        ]
      ],
      "weekStart": "string",
      "workCapacity": "string",
      "workingDays": [
        [
          "string"
        ]
      ],
      "workspaceNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `hasPassword` | boolean |  |
| `hasPendingApprovalRequest` | boolean |  |
| `imageUrl` | string |  |
| `name` | string |  |
| `userCustomFieldValues[]` | array |  |
| `weekStart` | string |  |
| `workCapacity` | string |  |
| `workingDays[]` | array<string> |  |
| `workspaceNumber` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/member-profile/:userId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-profile.md) for the provider-specific parameters and requirements.

