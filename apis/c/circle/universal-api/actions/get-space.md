# Circle: Get Space

Retrieves space details from Circle by ID.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-space?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/get-space?${params}`, {
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
| `id` | number | yes | Space ID |

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
      "isPostDisabled": "string",
      "isPrivate": "string",
      "lockedButtonLabel": "string",
      "lockedButtonUrl": "https://example.com",
      "lockedPageDescription": "string",
      "lockedPageHeading": "string",
      "lockScreenBlocks": "string",
      "name": "Ava Chen",
      "pinnedPostsLabel": "string",
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
| `isPostDisabled` | string |  |
| `isPrivate` | string |  |
| `lockedButtonLabel` | string |  |
| `lockedButtonUrl` | string |  |
| `lockedPageDescription` | string |  |
| `lockedPageHeading` | string |  |
| `lockScreenBlocks` | string |  |
| `name` | string |  |
| `pinnedPostsLabel` | string |  |
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

Through the native Circle API, this operation is `GET /api/admin/v2/spaces/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

