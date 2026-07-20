# Intercom: Update Conversation



```
PUT https://connect.mindcloud.co/v1/universal/intercom/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Intercom conversation identifier |
| `read` | boolean | no | Mark the conversation as read in Intercom |
| `title` | string | no | The title of the conversation |
| `customAttributes` | object | no | Custom attributes to update on the conversation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminAssigneeId": 1,
      "aiAgent": "string",
      "aiAgentParticipated": true,
      "company": "string",
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
      "conversationParts": {
        "conversationParts": [
          {
            "appPackageCode": "string",
            "assignedTo": "string",
            "attachments": [
              "string"
            ],
            "author": {
              "email": "ava@example.com",
              "fromAiAgent": true,
              "id": "string",
              "isAiAnswer": true,
              "name": "Ava Chen",
              "type": "string"
            },
            "body": "string",
            "createdAt": 1,
            "emailMessageMetadata": "ava@example.com",
            "eventDetails": {
              "attribute": {
                "name": "Ava Chen"
              },
              "value": {
                "name": "Ava Chen",
                "previous": "string"
              }
            },
            "externalId": "string",
            "id": "string",
            "metadata": {},
            "notifiedAt": 1,
            "partType": "string",
            "redacted": true,
            "state": "string",
            "tags": [
              "string"
            ],
            "type": "string",
            "updatedAt": 1
          }
        ],
        "totalCount": 1,
        "type": "string"
      },
      "conversationRating": "string",
      "createdAt": 1,
      "customAttributes": {
        "autoTranslated": true,
        "copilotUsed": true,
        "createdByAppPackageCode": "string",
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
        "firstAdminReplyAt": 1,
        "firstAssignmentAt": 1,
        "firstCloseAt": "string",
        "firstContactReplyAt": 1,
        "handlingTime": "string",
        "lastAdminReplyAt": 1,
        "lastAssignmentAdminReplyAt": 1,
        "lastAssignmentAt": 1,
        "lastCloseAt": "string",
        "lastClosedById": "string",
        "lastContactReplyAt": 1,
        "medianTimeToReply": 1,
        "timeToAdminReply": 1,
        "timeToAssignment": 1,
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
          {
            "id": "string",
            "type": "string"
          }
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
      "waitingSince": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminAssigneeId` | number |  |
| `aiAgent` | string |  |
| `aiAgentParticipated` | boolean |  |
| `company` | string |  |
| `contacts` | object |  |
| `contacts.contacts` | array<object> |  |
| `contacts.contacts[].externalId` | string |  |
| `contacts.contacts[].id` | string |  |
| `contacts.contacts[].type` | string |  |
| `contacts.type` | string |  |
| `conversationParts` | object |  |
| `conversationParts.conversationParts` | array<object> |  |
| `conversationParts.conversationParts[].appPackageCode` | string |  |
| `conversationParts.conversationParts[].assignedTo` | string |  |
| `conversationParts.conversationParts[].attachments` | array<string> |  |
| `conversationParts.conversationParts[].author` | object |  |
| `conversationParts.conversationParts[].author.email` | string |  |
| `conversationParts.conversationParts[].author.fromAiAgent` | boolean |  |
| `conversationParts.conversationParts[].author.id` | string |  |
| `conversationParts.conversationParts[].author.isAiAnswer` | boolean |  |
| `conversationParts.conversationParts[].author.name` | string |  |
| `conversationParts.conversationParts[].author.type` | string |  |
| `conversationParts.conversationParts[].body` | string |  |
| `conversationParts.conversationParts[].createdAt` | number |  |
| `conversationParts.conversationParts[].emailMessageMetadata` | string |  |
| `conversationParts.conversationParts[].eventDetails` | object |  |
| `conversationParts.conversationParts[].eventDetails.attribute` | object |  |
| `conversationParts.conversationParts[].eventDetails.attribute.name` | string |  |
| `conversationParts.conversationParts[].eventDetails.value` | object |  |
| `conversationParts.conversationParts[].eventDetails.value.name` | string |  |
| `conversationParts.conversationParts[].eventDetails.value.previous` | string |  |
| `conversationParts.conversationParts[].externalId` | string |  |
| `conversationParts.conversationParts[].id` | string |  |
| `conversationParts.conversationParts[].metadata` | object |  |
| `conversationParts.conversationParts[].notifiedAt` | number |  |
| `conversationParts.conversationParts[].partType` | string |  |
| `conversationParts.conversationParts[].redacted` | boolean |  |
| `conversationParts.conversationParts[].state` | string |  |
| `conversationParts.conversationParts[].tags` | array<string> |  |
| `conversationParts.conversationParts[].type` | string |  |
| `conversationParts.conversationParts[].updatedAt` | number |  |
| `conversationParts.totalCount` | number |  |
| `conversationParts.type` | string |  |
| `conversationRating` | string |  |
| `createdAt` | number |  |
| `customAttributes` | object |  |
| `customAttributes.autoTranslated` | boolean |  |
| `customAttributes.copilotUsed` | boolean |  |
| `customAttributes.createdByAppPackageCode` | string |  |
| `customAttributes.finAIAgentImageUsedInReply` | boolean |  |
| `customAttributes.finAIAgentPreview` | boolean |  |
| `customAttributes.hasAttachments` | boolean |  |
| `customAttributes.importedViaStandalone` | boolean |  |
| `customAttributes.language` | string |  |
| `firstContactReply` | object |  |
| `firstContactReply.createdAt` | number |  |
| `firstContactReply.type` | string |  |
| `firstContactReply.url` | string |  |
| `id` | string |  |
| `linkedObjects` | object |  |
| `linkedObjects.data` | array<string> |  |
| `linkedObjects.hasMore` | boolean |  |
| `linkedObjects.totalCount` | number |  |
| `linkedObjects.type` | string |  |
| `open` | boolean |  |
| `priority` | string |  |
| `read` | boolean |  |
| `slaApplied` | string |  |
| `snoozedUntil` | string |  |
| `source` | object |  |
| `source.attachments` | array<string> |  |
| `source.author` | object |  |
| `source.author.email` | string |  |
| `source.author.id` | string |  |
| `source.author.name` | string |  |
| `source.author.type` | string |  |
| `source.body` | string |  |
| `source.deliveredAs` | string |  |
| `source.id` | string |  |
| `source.recipients` | string |  |
| `source.redacted` | boolean |  |
| `source.subject` | string |  |
| `source.type` | string |  |
| `source.url` | string |  |
| `state` | string |  |
| `statistics` | object |  |
| `statistics.assignedTeamFirstResponseTime` | array<string> |  |
| `statistics.assignedTeamFirstResponseTimeInOfficeHours` | array<string> |  |
| `statistics.countAssignments` | number |  |
| `statistics.countConversationParts` | number |  |
| `statistics.countReopens` | number |  |
| `statistics.firstAdminReplyAt` | number |  |
| `statistics.firstAssignmentAt` | number |  |
| `statistics.firstCloseAt` | string |  |
| `statistics.firstContactReplyAt` | number |  |
| `statistics.handlingTime` | string |  |
| `statistics.lastAdminReplyAt` | number |  |
| `statistics.lastAssignmentAdminReplyAt` | number |  |
| `statistics.lastAssignmentAt` | number |  |
| `statistics.lastCloseAt` | string |  |
| `statistics.lastClosedById` | string |  |
| `statistics.lastContactReplyAt` | number |  |
| `statistics.medianTimeToReply` | number |  |
| `statistics.timeToAdminReply` | number |  |
| `statistics.timeToAssignment` | number |  |
| `statistics.timeToFirstClose` | string |  |
| `statistics.timeToLastClose` | string |  |
| `statistics.type` | string |  |
| `tags` | object |  |
| `tags.tags` | array<string> |  |
| `tags.type` | string |  |
| `teamAssigneeId` | string |  |
| `teammates` | object |  |
| `teammates.admins` | array<object> |  |
| `teammates.admins[].id` | string |  |
| `teammates.admins[].type` | string |  |
| `teammates.type` | string |  |
| `ticket` | string |  |
| `title` | string |  |
| `topics` | object |  |
| `topics.topics` | array<string> |  |
| `topics.totalCount` | number |  |
| `topics.type` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |
| `waitingSince` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `PUT /conversations/:conversation_id` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

