# Circle: List Space Members

Retrieves space membership records from Circle.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-space-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-space-members?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-space-members?${params}`, {
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
| `spaceId` | list<number> | yes | Space ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessType": "string",
      "communityMember": {
        "avatarUrl": "https://example.com",
        "communityId": 1,
        "email": "ava@example.com",
        "firstName": "Ava",
        "headline": "string",
        "lastName": "Chen",
        "name": "Ava Chen",
        "profileUrl": "https://example.com",
        "publicUid": "string"
      },
      "communityMemberId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "inAppNotificationSetting": "string",
      "mobileNotificationSetting": "string",
      "moderator": true,
      "notificationType": "string",
      "postsReadCount": 1,
      "spaceId": 1,
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessType` | string |  |
| `communityMember.avatarUrl` | string |  |
| `communityMember.communityId` | number |  |
| `communityMember.email` | string |  |
| `communityMember.firstName` | string |  |
| `communityMember.headline` | string |  |
| `communityMember.lastName` | string |  |
| `communityMember.name` | string |  |
| `communityMember.profileUrl` | string |  |
| `communityMember.publicUid` | string |  |
| `communityMemberId` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `inAppNotificationSetting` | string |  |
| `mobileNotificationSetting` | string |  |
| `moderator` | boolean |  |
| `notificationType` | string |  |
| `postsReadCount` | number |  |
| `spaceId` | number |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/space_members` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-space-members.md) for the provider-specific parameters and requirements.

