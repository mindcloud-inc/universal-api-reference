# Circle: Create Community Member

Creates a new community member in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email of the community member |
| `skipInvitation` | boolean | no | Skip sending invitation email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "communityMember": {
        "acceptedInvitation": "string",
        "active": true,
        "avatarUrl": "https://example.com",
        "commentsCount": 1,
        "communityId": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "flattenedProfileFields": {
          "bio": "string",
          "birthday": "string",
          "company": "string",
          "facebookUrl": "https://example.com",
          "headline": "string",
          "instagramUrl": "https://example.com",
          "linkedinUrl": "https://example.com",
          "location": "string",
          "profession": "string",
          "twitterUrl": "https://example.com",
          "website": "string"
        },
        "gamificationStats": "string",
        "headline": "string",
        "id": 1,
        "lastName": "Chen",
        "lastSeenAt": "string",
        "name": "Ava Chen",
        "postsCount": 1,
        "profileConfirmedAt": "string",
        "profileFields": [
          {
            "communityMemberProfileField": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "fieldType": "string",
            "id": 1,
            "key": "string",
            "label": "string",
            "numberOptions": "string",
            "pages": [
              {
                "createdAt": "2026-05-07T12:00:00.000Z",
                "id": 1,
                "name": "Ava Chen",
                "position": 1,
                "updatedAt": "2026-05-07T12:00:00.000Z",
                "visible": true
              }
            ],
            "placeholder": "string",
            "platformField": true,
            "required": true,
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
        ],
        "profileUrl": "https://example.com",
        "publicUid": "string",
        "ssoProviderUserId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communityMember.acceptedInvitation` | string |  |
| `communityMember.active` | boolean |  |
| `communityMember.avatarUrl` | string |  |
| `communityMember.commentsCount` | number |  |
| `communityMember.communityId` | number |  |
| `communityMember.createdAt` | date |  |
| `communityMember.email` | string |  |
| `communityMember.firstName` | string |  |
| `communityMember.flattenedProfileFields.bio` | string |  |
| `communityMember.flattenedProfileFields.birthday` | string |  |
| `communityMember.flattenedProfileFields.company` | string |  |
| `communityMember.flattenedProfileFields.facebookUrl` | string |  |
| `communityMember.flattenedProfileFields.headline` | string |  |
| `communityMember.flattenedProfileFields.instagramUrl` | string |  |
| `communityMember.flattenedProfileFields.linkedinUrl` | string |  |
| `communityMember.flattenedProfileFields.location` | string |  |
| `communityMember.flattenedProfileFields.profession` | string |  |
| `communityMember.flattenedProfileFields.twitterUrl` | string |  |
| `communityMember.flattenedProfileFields.website` | string |  |
| `communityMember.gamificationStats` | string |  |
| `communityMember.headline` | string |  |
| `communityMember.id` | number |  |
| `communityMember.lastName` | string |  |
| `communityMember.lastSeenAt` | string |  |
| `communityMember.name` | string |  |
| `communityMember.postsCount` | number |  |
| `communityMember.profileConfirmedAt` | string |  |
| `communityMember.profileFields[].communityMemberProfileField` | string |  |
| `communityMember.profileFields[].createdAt` | date |  |
| `communityMember.profileFields[].description` | string |  |
| `communityMember.profileFields[].fieldType` | string |  |
| `communityMember.profileFields[].id` | number |  |
| `communityMember.profileFields[].key` | string |  |
| `communityMember.profileFields[].label` | string |  |
| `communityMember.profileFields[].numberOptions` | string |  |
| `communityMember.profileFields[].pages[].createdAt` | date |  |
| `communityMember.profileFields[].pages[].id` | number |  |
| `communityMember.profileFields[].pages[].name` | string |  |
| `communityMember.profileFields[].pages[].position` | number |  |
| `communityMember.profileFields[].pages[].updatedAt` | date |  |
| `communityMember.profileFields[].pages[].visible` | boolean |  |
| `communityMember.profileFields[].placeholder` | string |  |
| `communityMember.profileFields[].platformField` | boolean |  |
| `communityMember.profileFields[].required` | boolean |  |
| `communityMember.profileFields[].updatedAt` | date |  |
| `communityMember.profileUrl` | string |  |
| `communityMember.publicUid` | string |  |
| `communityMember.ssoProviderUserId` | string |  |
| `communityMember.updatedAt` | date |  |
| `communityMember.userId` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/community_members` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-community-member.md) for the provider-specific parameters and requirements.

