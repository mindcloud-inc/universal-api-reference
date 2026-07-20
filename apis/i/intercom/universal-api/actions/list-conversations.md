# Intercom: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-conversations?${params}`, {
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
      "conversations": [
        {
          "adminAssigneeId": 1,
          "aiAgent": "string",
          "aiAgentParticipated": true,
          "company": {
            "appId": "string",
            "companyId": "string",
            "createdAt": 1,
            "customAttributes": {},
            "id": "string",
            "monthlySpend": 1,
            "name": "Ava Chen",
            "sessionCount": 1,
            "tagIds": [
              "string"
            ],
            "type": "string",
            "updatedAt": 1,
            "userCount": 1
          },
          "contacts": {
            "contacts": [
              {
                "externalId": "string",
                "id": "string",
                "type": "string"
              }
            ],
            "type": "string"
          },
          "conversationRating": "string",
          "createdAt": 1,
          "customAttributes": {
            "autoTranslated": true,
            "copilotUsed": true,
            "finAIAgentImageUsedInReply": true,
            "finAIAgentPreview": true,
            "hasAttachments": true,
            "importedViaStandalone": true,
            "language": "string"
          },
          "firstContactReply": {
            "createdAt": 1,
            "type": "string",
            "url": "https://example.com"
          },
          "id": "string",
          "linkedObjects": {
            "data": [
              "https://example.com"
            ],
            "hasMore": true,
            "totalCount": 1,
            "type": "https://example.com"
          },
          "open": true,
          "priority": "string",
          "read": true,
          "slaApplied": "string",
          "snoozedUntil": "string",
          "source": {
            "attachments": [
              "string"
            ],
            "author": {
              "email": "ava@example.com",
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "body": "string",
            "deliveredAs": "string",
            "id": "string",
            "recipients": "string",
            "redacted": true,
            "subject": "string",
            "type": "string",
            "url": "https://example.com"
          },
          "state": "string",
          "statistics": {
            "assignedTeamFirstResponseTime": [
              "string"
            ],
            "assignedTeamFirstResponseTimeInOfficeHours": [
              "string"
            ],
            "countAssignments": 1,
            "countConversationParts": 1,
            "countReopens": 1,
            "firstAdminReplyAt": "string",
            "firstAssignmentAt": "string",
            "firstCloseAt": "string",
            "firstContactReplyAt": 1,
            "handlingTime": "string",
            "lastAdminReplyAt": "string",
            "lastAssignmentAdminReplyAt": "string",
            "lastAssignmentAt": "string",
            "lastCloseAt": "string",
            "lastClosedById": "string",
            "lastContactReplyAt": 1,
            "medianTimeToReply": "string",
            "timeToAdminReply": "string",
            "timeToAssignment": "string",
            "timeToFirstClose": "string",
            "timeToLastClose": "string",
            "type": "string"
          },
          "tags": {
            "tags": [
              "string"
            ],
            "type": "string"
          },
          "teamAssigneeId": "string",
          "teammates": {
            "admins": [
              "string"
            ],
            "type": "string"
          },
          "ticket": "string",
          "title": "string",
          "topics": {
            "topics": [
              "string"
            ],
            "totalCount": 1,
            "type": "string"
          },
          "type": "string",
          "updatedAt": 1,
          "waitingSince": 1
        }
      ],
      "pages": {
        "page": 1,
        "perPage": "string",
        "totalPages": 1,
        "type": "string"
      },
      "totalCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversations` | array<object> |  |
| `conversations[].adminAssigneeId` | number |  |
| `conversations[].aiAgent` | string |  |
| `conversations[].aiAgentParticipated` | boolean |  |
| `conversations[].company` | object |  |
| `conversations[].company.appId` | string |  |
| `conversations[].company.companyId` | string |  |
| `conversations[].company.createdAt` | number |  |
| `conversations[].company.customAttributes` | object |  |
| `conversations[].company.id` | string |  |
| `conversations[].company.monthlySpend` | number |  |
| `conversations[].company.name` | string |  |
| `conversations[].company.sessionCount` | number |  |
| `conversations[].company.tagIds` | array<string> |  |
| `conversations[].company.type` | string |  |
| `conversations[].company.updatedAt` | number |  |
| `conversations[].company.userCount` | number |  |
| `conversations[].contacts` | object |  |
| `conversations[].contacts.contacts` | array<object> |  |
| `conversations[].contacts.contacts[].externalId` | string |  |
| `conversations[].contacts.contacts[].id` | string |  |
| `conversations[].contacts.contacts[].type` | string |  |
| `conversations[].contacts.type` | string |  |
| `conversations[].conversationRating` | string |  |
| `conversations[].createdAt` | number |  |
| `conversations[].customAttributes` | object |  |
| `conversations[].customAttributes.autoTranslated` | boolean |  |
| `conversations[].customAttributes.copilotUsed` | boolean |  |
| `conversations[].customAttributes.finAIAgentImageUsedInReply` | boolean |  |
| `conversations[].customAttributes.finAIAgentPreview` | boolean |  |
| `conversations[].customAttributes.hasAttachments` | boolean |  |
| `conversations[].customAttributes.importedViaStandalone` | boolean |  |
| `conversations[].customAttributes.language` | string |  |
| `conversations[].firstContactReply` | object |  |
| `conversations[].firstContactReply.createdAt` | number |  |
| `conversations[].firstContactReply.type` | string |  |
| `conversations[].firstContactReply.url` | string |  |
| `conversations[].id` | string |  |
| `conversations[].linkedObjects` | object |  |
| `conversations[].linkedObjects.data` | array<string> |  |
| `conversations[].linkedObjects.hasMore` | boolean |  |
| `conversations[].linkedObjects.totalCount` | number |  |
| `conversations[].linkedObjects.type` | string |  |
| `conversations[].open` | boolean |  |
| `conversations[].priority` | string |  |
| `conversations[].read` | boolean |  |
| `conversations[].slaApplied` | string |  |
| `conversations[].snoozedUntil` | string |  |
| `conversations[].source` | object |  |
| `conversations[].source.attachments` | array<string> |  |
| `conversations[].source.author` | object |  |
| `conversations[].source.author.email` | string |  |
| `conversations[].source.author.id` | string |  |
| `conversations[].source.author.name` | string |  |
| `conversations[].source.author.type` | string |  |
| `conversations[].source.body` | string |  |
| `conversations[].source.deliveredAs` | string |  |
| `conversations[].source.id` | string |  |
| `conversations[].source.recipients` | string |  |
| `conversations[].source.redacted` | boolean |  |
| `conversations[].source.subject` | string |  |
| `conversations[].source.type` | string |  |
| `conversations[].source.url` | string |  |
| `conversations[].state` | string |  |
| `conversations[].statistics` | object |  |
| `conversations[].statistics.assignedTeamFirstResponseTime` | array<string> |  |
| `conversations[].statistics.assignedTeamFirstResponseTimeInOfficeHours` | array<string> |  |
| `conversations[].statistics.countAssignments` | number |  |
| `conversations[].statistics.countConversationParts` | number |  |
| `conversations[].statistics.countReopens` | number |  |
| `conversations[].statistics.firstAdminReplyAt` | string |  |
| `conversations[].statistics.firstAssignmentAt` | string |  |
| `conversations[].statistics.firstCloseAt` | string |  |
| `conversations[].statistics.firstContactReplyAt` | number |  |
| `conversations[].statistics.handlingTime` | string |  |
| `conversations[].statistics.lastAdminReplyAt` | string |  |
| `conversations[].statistics.lastAssignmentAdminReplyAt` | string |  |
| `conversations[].statistics.lastAssignmentAt` | string |  |
| `conversations[].statistics.lastCloseAt` | string |  |
| `conversations[].statistics.lastClosedById` | string |  |
| `conversations[].statistics.lastContactReplyAt` | number |  |
| `conversations[].statistics.medianTimeToReply` | string |  |
| `conversations[].statistics.timeToAdminReply` | string |  |
| `conversations[].statistics.timeToAssignment` | string |  |
| `conversations[].statistics.timeToFirstClose` | string |  |
| `conversations[].statistics.timeToLastClose` | string |  |
| `conversations[].statistics.type` | string |  |
| `conversations[].tags` | object |  |
| `conversations[].tags.tags` | array<string> |  |
| `conversations[].tags.type` | string |  |
| `conversations[].teamAssigneeId` | string |  |
| `conversations[].teammates` | object |  |
| `conversations[].teammates.admins` | array<string> |  |
| `conversations[].teammates.type` | string |  |
| `conversations[].ticket` | string |  |
| `conversations[].title` | string |  |
| `conversations[].topics` | object |  |
| `conversations[].topics.topics` | array<string> |  |
| `conversations[].topics.totalCount` | number |  |
| `conversations[].topics.type` | string |  |
| `conversations[].type` | string |  |
| `conversations[].updatedAt` | number |  |
| `conversations[].waitingSince` | number |  |
| `pages` | object |  |
| `pages.page` | number |  |
| `pages.perPage` | string |  |
| `pages.totalPages` | number |  |
| `pages.type` | string |  |
| `totalCount` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `GET /conversations` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

