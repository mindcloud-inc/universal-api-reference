# Intercom: Convert Conversation To Ticket



```
PUT https://connect.mindcloud.co/v1/universal/intercom/latest/actions/convert-conversation-to-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/convert-conversation-to-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "ticket_type_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/convert-conversation-to-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "ticket_type_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Intercom conversation identifier |
| `ticket_type_id` | string | yes | Intercom ticket type identifier |
| `ticket_attributes` | object | no |  |
| `ticket_attributes._default_title_` | string | no | Default converted ticket title |
| `ticket_attributes._default_description_` | string | no | Default converted ticket description |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminAssigneeId": "string",
      "category": "string",
      "channel": "string",
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
      "createdAt": 1,
      "id": "string",
      "isShared": true,
      "linkedObjects": {
        "data": [
          "https://example.com"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "https://example.com"
      },
      "open": true,
      "teamAssigneeId": "string",
      "ticketAttributes": {
        "defaultDescription": "string",
        "defaultTitle": "string",
        "platforms": "string",
        "rootCause": "string"
      },
      "ticketId": "string",
      "ticketParts": {
        "ticketParts": [
          {
            "attachments": [
              "string"
            ],
            "author": {
              "email": "ava@example.com",
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "createdAt": 1,
            "id": "string",
            "partType": "string",
            "redacted": true,
            "type": "string",
            "updatedAt": 1,
            "updatedAttributeData": {
              "attribute": {
                "id": "string",
                "label": "string",
                "type": "string"
              },
              "value": {
                "id": "string",
                "label": "string",
                "previous": "string",
                "type": "string"
              }
            }
          }
        ],
        "totalCount": 1,
        "type": "string"
      },
      "ticketState": {
        "category": "string",
        "externalLabel": "string",
        "id": "string",
        "internalLabel": "string",
        "type": "string"
      },
      "ticketType": {
        "archived": true,
        "category": "string",
        "createdAt": 1,
        "description": "string",
        "icon": "string",
        "id": "string",
        "isInternal": true,
        "name": "Ava Chen",
        "ticketTypeAttributes": {
          "data": [
            {
              "archived": true,
              "createdAt": 1,
              "dataType": "string",
              "default": true,
              "description": "string",
              "id": "string",
              "inputOptions": {
                "multiline": true
              },
              "name": "Ava Chen",
              "order": 1,
              "requiredToCreate": true,
              "requiredToCreateForContacts": true,
              "ticketTypeId": 1,
              "type": "string",
              "updatedAt": 1,
              "visibleOnCreate": true,
              "visibleToContacts": true,
              "workspaceId": "string"
            }
          ],
          "type": "string"
        },
        "type": "string",
        "updatedAt": 1,
        "workspaceId": "string"
      },
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminAssigneeId` | string |  |
| `category` | string |  |
| `channel` | string |  |
| `contacts` | object |  |
| `contacts.contacts` | array<object> |  |
| `contacts.contacts[].externalId` | string |  |
| `contacts.contacts[].id` | string |  |
| `contacts.contacts[].type` | string |  |
| `contacts.type` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `isShared` | boolean |  |
| `linkedObjects` | object |  |
| `linkedObjects.data` | array<string> |  |
| `linkedObjects.hasMore` | boolean |  |
| `linkedObjects.totalCount` | number |  |
| `linkedObjects.type` | string |  |
| `open` | boolean |  |
| `teamAssigneeId` | string |  |
| `ticketAttributes` | object |  |
| `ticketAttributes.defaultDescription` | string |  |
| `ticketAttributes.defaultTitle` | string |  |
| `ticketAttributes.platforms` | string |  |
| `ticketAttributes.rootCause` | string |  |
| `ticketId` | string |  |
| `ticketParts` | object |  |
| `ticketParts.ticketParts` | array<object> |  |
| `ticketParts.ticketParts[].attachments` | array<string> |  |
| `ticketParts.ticketParts[].author` | object |  |
| `ticketParts.ticketParts[].author.email` | string |  |
| `ticketParts.ticketParts[].author.id` | string |  |
| `ticketParts.ticketParts[].author.name` | string |  |
| `ticketParts.ticketParts[].author.type` | string |  |
| `ticketParts.ticketParts[].createdAt` | number |  |
| `ticketParts.ticketParts[].id` | string |  |
| `ticketParts.ticketParts[].partType` | string |  |
| `ticketParts.ticketParts[].redacted` | boolean |  |
| `ticketParts.ticketParts[].type` | string |  |
| `ticketParts.ticketParts[].updatedAt` | number |  |
| `ticketParts.ticketParts[].updatedAttributeData` | object |  |
| `ticketParts.ticketParts[].updatedAttributeData.attribute` | object |  |
| `ticketParts.ticketParts[].updatedAttributeData.attribute.id` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.attribute.label` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.attribute.type` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.value` | object |  |
| `ticketParts.ticketParts[].updatedAttributeData.value.id` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.value.label` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.value.previous` | string |  |
| `ticketParts.ticketParts[].updatedAttributeData.value.type` | string |  |
| `ticketParts.totalCount` | number |  |
| `ticketParts.type` | string |  |
| `ticketState` | object |  |
| `ticketState.category` | string |  |
| `ticketState.externalLabel` | string |  |
| `ticketState.id` | string |  |
| `ticketState.internalLabel` | string |  |
| `ticketState.type` | string |  |
| `ticketType` | object |  |
| `ticketType.archived` | boolean |  |
| `ticketType.category` | string |  |
| `ticketType.createdAt` | number |  |
| `ticketType.description` | string |  |
| `ticketType.icon` | string |  |
| `ticketType.id` | string |  |
| `ticketType.isInternal` | boolean |  |
| `ticketType.name` | string |  |
| `ticketType.ticketTypeAttributes` | object |  |
| `ticketType.ticketTypeAttributes.data` | array<object> |  |
| `ticketType.ticketTypeAttributes.data[].archived` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].createdAt` | number |  |
| `ticketType.ticketTypeAttributes.data[].dataType` | string |  |
| `ticketType.ticketTypeAttributes.data[].default` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].description` | string |  |
| `ticketType.ticketTypeAttributes.data[].id` | string |  |
| `ticketType.ticketTypeAttributes.data[].inputOptions` | object |  |
| `ticketType.ticketTypeAttributes.data[].inputOptions.multiline` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].name` | string |  |
| `ticketType.ticketTypeAttributes.data[].order` | number |  |
| `ticketType.ticketTypeAttributes.data[].requiredToCreate` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].requiredToCreateForContacts` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].ticketTypeId` | number |  |
| `ticketType.ticketTypeAttributes.data[].type` | string |  |
| `ticketType.ticketTypeAttributes.data[].updatedAt` | number |  |
| `ticketType.ticketTypeAttributes.data[].visibleOnCreate` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].visibleToContacts` | boolean |  |
| `ticketType.ticketTypeAttributes.data[].workspaceId` | string |  |
| `ticketType.ticketTypeAttributes.type` | string |  |
| `ticketType.type` | string |  |
| `ticketType.updatedAt` | number |  |
| `ticketType.workspaceId` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /conversations/:conversation_id/convert` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-conversation-to-ticket.md) for the provider-specific parameters and requirements.

