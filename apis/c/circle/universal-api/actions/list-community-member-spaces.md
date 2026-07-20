# Circle: List Community Member Spaces

Retrieves community member space memberships from Circle.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-member-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-member-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-member-spaces?${params}`, {
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
      "communityId": 1,
      "coverImageDisplayStyle": "string",
      "coverImageUrl": "https://example.com",
      "coverImageVisible": true,
      "customEmojiDarkUrl": "https://example.com",
      "customEmojiUrl": "https://example.com",
      "defaultCommentSort": "string",
      "defaultInAppNotificationSetting": "string",
      "defaultMemberSort": "string",
      "defaultMentionInAppNotificationSetting": "string",
      "defaultMentionMobileNotificationSetting": "string",
      "defaultMobileNotificationSetting": "string",
      "defaultNotificationSetting": "string",
      "defaultSort": "string",
      "defaultTab": "string",
      "disableMemberPostCovers": "string",
      "displayView": "string",
      "emoji": "string",
      "eventAutoRsvpEnabled": true,
      "hideFromFeaturedAreas": true,
      "hideFromSidebar": true,
      "hideMembersCount": "string",
      "hidePostSettings": "string",
      "hideRightSidebar": true,
      "hideSorting": "string",
      "host": "string",
      "id": 1,
      "isHidden": true,
      "isHiddenFromNonMembers": true,
      "isPostDisabled": true,
      "isPrivate": true,
      "lockedButtonLabel": "string",
      "lockedButtonUrl": "https://example.com",
      "lockedPageDescription": "string",
      "lockedPageHeading": "string",
      "lockScreenBlocks": "string",
      "name": "Ava Chen",
      "pinnedPostsLabel": "string",
      "postIds": [
        1
      ],
      "preventMembersFromAddingOthers": true,
      "requireTopicSelection": true,
      "showLockIconForNonMembers": true,
      "showNextEvent": true,
      "showTabBar": true,
      "slug": "string",
      "spaceGroup": {
        "id": 1,
        "name": "Ava Chen"
      },
      "spaceType": "string",
      "thumbnailImageUrl": "https://example.com",
      "url": "https://example.com",
      "visibleTabs": {
        "members": true,
        "posts": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communityId` | number |  |
| `coverImageDisplayStyle` | string |  |
| `coverImageUrl` | string |  |
| `coverImageVisible` | boolean |  |
| `customEmojiDarkUrl` | string |  |
| `customEmojiUrl` | string |  |
| `defaultCommentSort` | string |  |
| `defaultInAppNotificationSetting` | string |  |
| `defaultMemberSort` | string |  |
| `defaultMentionInAppNotificationSetting` | string |  |
| `defaultMentionMobileNotificationSetting` | string |  |
| `defaultMobileNotificationSetting` | string |  |
| `defaultNotificationSetting` | string |  |
| `defaultSort` | string |  |
| `defaultTab` | string |  |
| `disableMemberPostCovers` | string |  |
| `displayView` | string |  |
| `emoji` | string |  |
| `eventAutoRsvpEnabled` | boolean |  |
| `hideFromFeaturedAreas` | boolean |  |
| `hideFromSidebar` | boolean |  |
| `hideMembersCount` | string |  |
| `hidePostSettings` | string |  |
| `hideRightSidebar` | boolean |  |
| `hideSorting` | string |  |
| `host` | string |  |
| `id` | number |  |
| `isHidden` | boolean |  |
| `isHiddenFromNonMembers` | boolean |  |
| `isPostDisabled` | boolean |  |
| `isPrivate` | boolean |  |
| `lockedButtonLabel` | string |  |
| `lockedButtonUrl` | string |  |
| `lockedPageDescription` | string |  |
| `lockedPageHeading` | string |  |
| `lockScreenBlocks` | string |  |
| `name` | string |  |
| `pinnedPostsLabel` | string |  |
| `postIds` | array<number> |  |
| `preventMembersFromAddingOthers` | boolean |  |
| `requireTopicSelection` | boolean |  |
| `showLockIconForNonMembers` | boolean |  |
| `showNextEvent` | boolean |  |
| `showTabBar` | boolean |  |
| `slug` | string |  |
| `spaceGroup.id` | number |  |
| `spaceGroup.name` | string |  |
| `spaceType` | string |  |
| `thumbnailImageUrl` | string |  |
| `url` | string |  |
| `visibleTabs.members` | boolean |  |
| `visibleTabs.posts` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/community_member_spaces` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-community-member-spaces.md) for the provider-specific parameters and requirements.

