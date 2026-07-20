# Google Groups: Get Group Settings

Retrieves settings for a group in Google Groups.

```
GET https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group-settings?connectionId=$CONNECTION_ID&groupUniqueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupUniqueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group-settings?${params}`, {
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
| `groupUniqueId` | string | yes | The group email address used by the Groups Settings API. |

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

Through the native Google Groups API, this operation is `GET https://www.googleapis.com/groups/v1/groups/:groupUniqueId` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-settings.md) for the provider-specific parameters and requirements.

