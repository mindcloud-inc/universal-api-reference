# Update Group Settings with Google Groups

Replaces group settings in Google Groups.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://www.googleapis.com/groups/v1/groups/:groupUniqueId`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Update Group Settings](https://developers.google.com/workspace/admin/groups-settings/v1/reference/groups/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupUniqueId` | path | `string` | yes | The group email address used by the Groups Settings API. |
| `name` | body | `string` | no | The group's display name in Google Groups settings. |
| `description` | body | `string` | no | The group's description in Google Groups settings. |
| `whoCanJoin` | body | `string` | no | Who can join the group. |
| `whoCanViewMembership` | body | `string` | no | Who can view the group's membership list. |
| `whoCanViewGroup` | body | `string` | no | Who can view the group's messages. |
| `allowExternalMembers` | body | `string` | no | Whether external members are allowed in the group. |
| `whoCanPostMessage` | body | `string` | no | Who can post messages to the group. |
| `allowWebPosting` | body | `string` | no | Whether posting from the web UI is allowed. |
| `primaryLanguage` | body | `string` | no | The group's primary language tag. |
| `isArchived` | body | `string` | no | Whether group messages are archived. |
| `messageModerationLevel` | body | `string` | no | How new messages are moderated. |
| `whoCanModerateMembers` | body | `string` | no | Who can manage group members. |
| `whoCanModerateContent` | body | `string` | no | Who can moderate group content. |
| `enableCollaborativeInbox` | body | `string` | no | Whether collaborative inbox is enabled for the group. |
| `showInGroupDirectory` | body | `string` | no | Whether the group appears in the group directory. |
| `whoCanDiscoverGroup` | body | `string` | no | Who can discover the group. |
| `defaultSender` | body | `string` | no | The default sender identity for members who can post as the group. |
