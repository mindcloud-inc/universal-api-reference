# Circle: Get Community Member

Retrieves community member details from Circle by ID.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-community-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-community-member?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-community-member?${params}`, {
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
| `id` | number | yes | Community member ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedInvitation": "2026-05-07T12:00:00.000Z",
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
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "postsCount": 1,
      "profileConfirmedAt": "2026-05-07T12:00:00.000Z",
      "profileFields": [
        {
          "communityMemberProfileField": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "displayValue": "string",
            "id": 1,
            "text": "string",
            "textarea": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          },
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedInvitation` | date |  |
| `active` | boolean |  |
| `avatarUrl` | string |  |
| `commentsCount` | number |  |
| `communityId` | number |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `flattenedProfileFields.bio` | string |  |
| `flattenedProfileFields.birthday` | string |  |
| `flattenedProfileFields.company` | string |  |
| `flattenedProfileFields.facebookUrl` | string |  |
| `flattenedProfileFields.headline` | string |  |
| `flattenedProfileFields.instagramUrl` | string |  |
| `flattenedProfileFields.linkedinUrl` | string |  |
| `flattenedProfileFields.location` | string |  |
| `flattenedProfileFields.profession` | string |  |
| `flattenedProfileFields.twitterUrl` | string |  |
| `flattenedProfileFields.website` | string |  |
| `gamificationStats` | string |  |
| `headline` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `lastSeenAt` | date |  |
| `name` | string |  |
| `postsCount` | number |  |
| `profileConfirmedAt` | date |  |
| `profileFields[].communityMemberProfileField.createdAt` | date |  |
| `profileFields[].communityMemberProfileField.displayValue` | string |  |
| `profileFields[].communityMemberProfileField.id` | number |  |
| `profileFields[].communityMemberProfileField.text` | string |  |
| `profileFields[].communityMemberProfileField.textarea` | string |  |
| `profileFields[].communityMemberProfileField.updatedAt` | date |  |
| `profileFields[].createdAt` | date |  |
| `profileFields[].description` | string |  |
| `profileFields[].fieldType` | string |  |
| `profileFields[].id` | number |  |
| `profileFields[].key` | string |  |
| `profileFields[].label` | string |  |
| `profileFields[].numberOptions` | string |  |
| `profileFields[].pages[].createdAt` | date |  |
| `profileFields[].pages[].id` | number |  |
| `profileFields[].pages[].name` | string |  |
| `profileFields[].pages[].position` | number |  |
| `profileFields[].pages[].updatedAt` | date |  |
| `profileFields[].pages[].visible` | boolean |  |
| `profileFields[].placeholder` | string |  |
| `profileFields[].platformField` | boolean |  |
| `profileFields[].required` | boolean |  |
| `profileFields[].updatedAt` | date |  |
| `profileUrl` | string |  |
| `publicUid` | string |  |
| `ssoProviderUserId` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/community_members/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-community-member.md) for the provider-specific parameters and requirements.

