# Intercom: Get Ticket



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | string | yes | Intercom ticket identifier |

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
            "previousTicketState": "string",
            "redacted": true,
            "ticketState": "string",
            "type": "string",
            "updatedAt": 1
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
| `ticketParts.ticketParts[].previousTicketState` | string |  |
| `ticketParts.ticketParts[].redacted` | boolean |  |
| `ticketParts.ticketParts[].ticketState` | string |  |
| `ticketParts.ticketParts[].type` | string |  |
| `ticketParts.ticketParts[].updatedAt` | number |  |
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

Through the native Intercom API, this operation is `GET /tickets/:ticket_id` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

