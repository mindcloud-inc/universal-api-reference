# Circle: Update Community

Updates current community details in Circle.

```
PUT https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-community
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-community" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "community": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-community', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "community": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `community` | object | yes | Community update payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowSignupsToPublicCommunity": true,
      "communitySetting": {
        "allowMembersToGoLive": true,
        "allowModeratorCsvDownload": true,
        "allowProfileSearchIndexing": true,
        "communityActivityNotificationsEmailEnabled": true,
        "communityActivityNotificationsInAppEnabled": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deactivateAccountEnabled": true,
        "defaultLoggedOutRedirectId": "string",
        "defaultLoggedOutRedirectType": "string",
        "desktopAppCommunityVisibilityEnabled": true,
        "enforceOtpForSignup": true,
        "hideEmailsOnMemberProfiles": true,
        "id": 1,
        "iosAppEnabled": true,
        "memberMediaUploadsEnabled": true,
        "showIosAppBanner": true,
        "truncatePostBodyInEmailNotifications": true,
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "communitySwitcherEnabled": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customCtaForShareLinks": true,
      "customTos": "string",
      "customTosEnabled": true,
      "defaultExistingMemberSpaceId": "string",
      "defaultLoggedOutSpaceId": "string",
      "defaultNewMemberSpaceId": "string",
      "defaultSearchSorting": "string",
      "digestIntro": "string",
      "digestsHideComments": "string",
      "digestsHideMembers": "string",
      "digestsHidePosts": "string",
      "digestsHideStats": "string",
      "digestSubject": "string",
      "id": 1,
      "isPrivate": true,
      "locale": "string",
      "lockedPostCtaBody": "string",
      "lockedPostCtaButtonText": "string",
      "lockedPostCtaButtonUrl": "https://example.com",
      "lockedPostCtaHeading": "string",
      "name": "Ava Chen",
      "prefs": {
        "brandColor": {
          "dark": "string",
          "light": "string"
        },
        "brandTextColor": {
          "dark": "string",
          "light": "string"
        },
        "hasInvitedMember": true,
        "hasPosts": true,
        "hasSpaces": true
      },
      "privateSignupLinkLabel": "https://example.com",
      "privateSignupLinkUrl": "https://example.com",
      "replyToEmail": "ava@example.com",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "weeklyDigestEnabled": true,
      "whiteLabel": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowSignupsToPublicCommunity` | boolean |  |
| `communitySetting.allowMembersToGoLive` | boolean |  |
| `communitySetting.allowModeratorCsvDownload` | boolean |  |
| `communitySetting.allowProfileSearchIndexing` | boolean |  |
| `communitySetting.communityActivityNotificationsEmailEnabled` | boolean |  |
| `communitySetting.communityActivityNotificationsInAppEnabled` | boolean |  |
| `communitySetting.createdAt` | date |  |
| `communitySetting.deactivateAccountEnabled` | boolean |  |
| `communitySetting.defaultLoggedOutRedirectId` | string |  |
| `communitySetting.defaultLoggedOutRedirectType` | string |  |
| `communitySetting.desktopAppCommunityVisibilityEnabled` | boolean |  |
| `communitySetting.enforceOtpForSignup` | boolean |  |
| `communitySetting.hideEmailsOnMemberProfiles` | boolean |  |
| `communitySetting.id` | number |  |
| `communitySetting.iosAppEnabled` | boolean |  |
| `communitySetting.memberMediaUploadsEnabled` | boolean |  |
| `communitySetting.showIosAppBanner` | boolean |  |
| `communitySetting.truncatePostBodyInEmailNotifications` | boolean |  |
| `communitySetting.updatedAt` | date |  |
| `communitySwitcherEnabled` | boolean |  |
| `createdAt` | date |  |
| `customCtaForShareLinks` | boolean |  |
| `customTos` | string |  |
| `customTosEnabled` | boolean |  |
| `defaultExistingMemberSpaceId` | string |  |
| `defaultLoggedOutSpaceId` | string |  |
| `defaultNewMemberSpaceId` | string |  |
| `defaultSearchSorting` | string |  |
| `digestIntro` | string |  |
| `digestsHideComments` | string |  |
| `digestsHideMembers` | string |  |
| `digestsHidePosts` | string |  |
| `digestsHideStats` | string |  |
| `digestSubject` | string |  |
| `id` | number |  |
| `isPrivate` | boolean |  |
| `locale` | string |  |
| `lockedPostCtaBody` | string |  |
| `lockedPostCtaButtonText` | string |  |
| `lockedPostCtaButtonUrl` | string |  |
| `lockedPostCtaHeading` | string |  |
| `name` | string |  |
| `prefs.brandColor.dark` | string |  |
| `prefs.brandColor.light` | string |  |
| `prefs.brandTextColor.dark` | string |  |
| `prefs.brandTextColor.light` | string |  |
| `prefs.hasInvitedMember` | boolean |  |
| `prefs.hasPosts` | boolean |  |
| `prefs.hasSpaces` | boolean |  |
| `privateSignupLinkLabel` | string |  |
| `privateSignupLinkUrl` | string |  |
| `replyToEmail` | string |  |
| `slug` | string |  |
| `updatedAt` | date |  |
| `weeklyDigestEnabled` | boolean |  |
| `whiteLabel` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `PUT /api/admin/v2/community` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-community.md) for the provider-specific parameters and requirements.

