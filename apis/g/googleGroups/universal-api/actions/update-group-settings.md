# Google Groups: Update Group Settings

Replaces group settings in Google Groups.

```
PUT https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupUniqueId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupUniqueId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupUniqueId` | string | yes | The group email address used by the Groups Settings API. |
| `name` | string | no | The group's display name in Google Groups settings. |
| `description` | string | no | The group's description in Google Groups settings. |
| `whoCanJoin` | string | no | Who can join the group. |
| `whoCanViewMembership` | string | no | Who can view the group's membership list. |
| `whoCanViewGroup` | string | no | Who can view the group's messages. |
| `allowExternalMembers` | string | no | Whether external members are allowed in the group. |
| `whoCanPostMessage` | string | no | Who can post messages to the group. |
| `allowWebPosting` | string | no | Whether posting from the web UI is allowed. |
| `primaryLanguage` | string | no | The group's primary language tag. |
| `isArchived` | string | no | Whether group messages are archived. |
| `messageModerationLevel` | string | no | How new messages are moderated. |
| `whoCanModerateMembers` | string | no | Who can manage group members. |
| `whoCanModerateContent` | string | no | Who can moderate group content. |
| `enableCollaborativeInbox` | string | no | Whether collaborative inbox is enabled for the group. |
| `showInGroupDirectory` | string | no | Whether the group appears in the group directory. |
| `whoCanDiscoverGroup` | string | no | Who can discover the group. |
| `defaultSender` | string | no | The default sender identity for members who can post as the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowExternalMembers": "string",
      "allowWebPosting": "string",
      "defaultSender": "string",
      "description": "string",
      "email": "ava@example.com",
      "enableCollaborativeInbox": "string",
      "isArchived": "string",
      "kind": "string",
      "messageModerationLevel": "string",
      "name": "Ava Chen",
      "primaryLanguage": "string",
      "showInGroupDirectory": "string",
      "whoCanDiscoverGroup": "string",
      "whoCanJoin": "string",
      "whoCanModerateContent": "string",
      "whoCanModerateMembers": "string",
      "whoCanPostMessage": "string",
      "whoCanViewGroup": "string",
      "whoCanViewMembership": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowExternalMembers` | string | Whether external members are allowed. |
| `allowWebPosting` | string | Whether web posting is allowed. |
| `defaultSender` | string | The default sender identity for the group. |
| `description` | string | The group's description. |
| `email` | string | The group's email address. |
| `enableCollaborativeInbox` | string | Whether collaborative inbox is enabled. |
| `isArchived` | string | Whether messages are archived. |
| `kind` | string | Always groupsSettings#groups. |
| `messageModerationLevel` | string | How new messages are moderated. |
| `name` | string | The group's display name. |
| `primaryLanguage` | string | The group's primary language. |
| `showInGroupDirectory` | string | Whether the group is shown in the directory. |
| `whoCanDiscoverGroup` | string | Who can discover the group. |
| `whoCanJoin` | string | Permission to join the group. |
| `whoCanModerateContent` | string | Who can moderate group content. |
| `whoCanModerateMembers` | string | Who can manage group members. |
| `whoCanPostMessage` | string | Who can post messages to the group. |
| `whoCanViewGroup` | string | Who can view the group's conversations. |
| `whoCanViewMembership` | string | Who can view the membership list. |

## Native endpoint

Through the native Google Groups API, this operation is `PUT https://www.googleapis.com/groups/v1/groups/:groupUniqueId` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-settings.md) for the provider-specific parameters and requirements.

