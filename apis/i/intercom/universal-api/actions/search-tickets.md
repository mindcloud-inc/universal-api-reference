# Intercom: Search Tickets



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0&query.field=string&query.operator=string&query.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query.field": "string",
  "query.operator": "string",
  "query.value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-tickets?${params}`, {
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
| `query` | object | no |  |
| `query.field` | string | yes | Field to search by |
| `query.operator` | string | yes | Search operator |
| `query.value` | string | yes | Value to match |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": {
        "page": 1,
        "perPage": 1,
        "totalPages": 1,
        "type": "string"
      },
      "tickets": [
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
| `pages` | object |  |
| `pages.page` | number |  |
| `pages.perPage` | number |  |
| `pages.totalPages` | number |  |
| `pages.type` | string |  |
| `tickets` | array<object> |  |
| `tickets[].adminAssigneeId` | string |  |
| `tickets[].category` | string |  |
| `tickets[].channel` | string |  |
| `tickets[].contacts` | object |  |
| `tickets[].contacts.contacts` | array<object> |  |
| `tickets[].contacts.contacts[].externalId` | string |  |
| `tickets[].contacts.contacts[].id` | string |  |
| `tickets[].contacts.contacts[].type` | string |  |
| `tickets[].contacts.type` | string |  |
| `tickets[].createdAt` | number |  |
| `tickets[].id` | string |  |
| `tickets[].isShared` | boolean |  |
| `tickets[].linkedObjects` | object |  |
| `tickets[].linkedObjects.data` | array<string> |  |
| `tickets[].linkedObjects.hasMore` | boolean |  |
| `tickets[].linkedObjects.totalCount` | number |  |
| `tickets[].linkedObjects.type` | string |  |
| `tickets[].open` | boolean |  |
| `tickets[].teamAssigneeId` | string |  |
| `tickets[].ticketAttributes` | object |  |
| `tickets[].ticketAttributes.defaultDescription` | string |  |
| `tickets[].ticketAttributes.defaultTitle` | string |  |
| `tickets[].ticketAttributes.platforms` | string |  |
| `tickets[].ticketAttributes.rootCause` | string |  |
| `tickets[].ticketId` | string |  |
| `tickets[].ticketParts` | object |  |
| `tickets[].ticketParts.ticketParts` | array<object> |  |
| `tickets[].ticketParts.ticketParts[].attachments` | array<string> |  |
| `tickets[].ticketParts.ticketParts[].author` | object |  |
| `tickets[].ticketParts.ticketParts[].author.email` | string |  |
| `tickets[].ticketParts.ticketParts[].author.id` | string |  |
| `tickets[].ticketParts.ticketParts[].author.name` | string |  |
| `tickets[].ticketParts.ticketParts[].author.type` | string |  |
| `tickets[].ticketParts.ticketParts[].createdAt` | number |  |
| `tickets[].ticketParts.ticketParts[].id` | string |  |
| `tickets[].ticketParts.ticketParts[].partType` | string |  |
| `tickets[].ticketParts.ticketParts[].previousTicketState` | string |  |
| `tickets[].ticketParts.ticketParts[].redacted` | boolean |  |
| `tickets[].ticketParts.ticketParts[].ticketState` | string |  |
| `tickets[].ticketParts.ticketParts[].type` | string |  |
| `tickets[].ticketParts.ticketParts[].updatedAt` | number |  |
| `tickets[].ticketParts.totalCount` | number |  |
| `tickets[].ticketParts.type` | string |  |
| `tickets[].ticketState` | object |  |
| `tickets[].ticketState.category` | string |  |
| `tickets[].ticketState.externalLabel` | string |  |
| `tickets[].ticketState.id` | string |  |
| `tickets[].ticketState.internalLabel` | string |  |
| `tickets[].ticketState.type` | string |  |
| `tickets[].ticketType` | object |  |
| `tickets[].ticketType.archived` | boolean |  |
| `tickets[].ticketType.category` | string |  |
| `tickets[].ticketType.createdAt` | number |  |
| `tickets[].ticketType.description` | string |  |
| `tickets[].ticketType.icon` | string |  |
| `tickets[].ticketType.id` | string |  |
| `tickets[].ticketType.isInternal` | boolean |  |
| `tickets[].ticketType.name` | string |  |
| `tickets[].ticketType.ticketTypeAttributes` | object |  |
| `tickets[].ticketType.ticketTypeAttributes.data` | array<object> |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].archived` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].createdAt` | number |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].dataType` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].default` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].description` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].id` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].inputOptions` | object |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].inputOptions.multiline` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].name` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].order` | number |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].requiredToCreate` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].requiredToCreateForContacts` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].ticketTypeId` | number |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].type` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].updatedAt` | number |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].visibleOnCreate` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].visibleToContacts` | boolean |  |
| `tickets[].ticketType.ticketTypeAttributes.data[].workspaceId` | string |  |
| `tickets[].ticketType.ticketTypeAttributes.type` | string |  |
| `tickets[].ticketType.type` | string |  |
| `tickets[].ticketType.updatedAt` | number |  |
| `tickets[].ticketType.workspaceId` | string |  |
| `tickets[].type` | string |  |
| `tickets[].updatedAt` | number |  |
| `totalCount` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /tickets/search` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

