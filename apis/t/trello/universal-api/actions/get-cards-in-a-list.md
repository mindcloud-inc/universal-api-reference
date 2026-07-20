# Trello: Get Cards in a List

Retrieves cards in a list from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-cards-in-a-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-cards-in-a-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-cards-in-a-list?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "badges": {
        "attachments": 1,
        "attachmentsByType": {
          "trello": {
            "board": 1,
            "card": 1
          }
        },
        "checkItems": 1,
        "checkItemsChecked": 1,
        "checkItemsEarliestDue": {},
        "comments": 1,
        "description": true,
        "due": {},
        "dueComplete": true,
        "externalSource": {},
        "fogbugz": "string",
        "lastUpdatedByAi": true,
        "location": true,
        "maliciousAttachments": 1,
        "start": {},
        "subscribed": true,
        "viewingMemberVoted": true,
        "votes": 1
      },
      "cardRole": {},
      "closed": true,
      "cover": {
        "brightness": "string",
        "color": {},
        "idAttachment": {},
        "idPlugin": {},
        "idUploadedBackground": {},
        "size": "string",
        "yPosition": 1
      },
      "dateLastActivity": "string",
      "desc": "string",
      "due": {},
      "dueComplete": true,
      "dueReminder": {},
      "email": {},
      "id": "string",
      "idAttachmentCover": {},
      "idBoard": "string",
      "idList": "string",
      "idShort": 1,
      "isTemplate": true,
      "manualCoverAttachment": true,
      "mirrorSourceId": {},
      "name": "Ava Chen",
      "nodeId": "string",
      "pinned": true,
      "pos": 1,
      "shortLink": "https://example.com",
      "shortUrl": "https://example.com",
      "start": {},
      "subscribed": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `badges.attachments` | number |  |
| `badges.attachmentsByType.trello.board` | number |  |
| `badges.attachmentsByType.trello.card` | number |  |
| `badges.checkItems` | number |  |
| `badges.checkItemsChecked` | number |  |
| `badges.checkItemsEarliestDue` | object |  |
| `badges.comments` | number |  |
| `badges.description` | boolean |  |
| `badges.due` | object |  |
| `badges.dueComplete` | boolean |  |
| `badges.externalSource` | object |  |
| `badges.fogbugz` | string |  |
| `badges.lastUpdatedByAi` | boolean |  |
| `badges.location` | boolean |  |
| `badges.maliciousAttachments` | number |  |
| `badges.start` | object |  |
| `badges.subscribed` | boolean |  |
| `badges.viewingMemberVoted` | boolean |  |
| `badges.votes` | number |  |
| `cardRole` | object |  |
| `closed` | boolean |  |
| `cover.brightness` | string |  |
| `cover.color` | object |  |
| `cover.idAttachment` | object |  |
| `cover.idPlugin` | object |  |
| `cover.idUploadedBackground` | object |  |
| `cover.size` | string |  |
| `cover.yPosition` | number |  |
| `dateLastActivity` | string |  |
| `desc` | string |  |
| `due` | object |  |
| `dueComplete` | boolean |  |
| `dueReminder` | object |  |
| `email` | object |  |
| `id` | string |  |
| `idAttachmentCover` | object |  |
| `idBoard` | string |  |
| `idList` | string |  |
| `idShort` | number |  |
| `isTemplate` | boolean |  |
| `manualCoverAttachment` | boolean |  |
| `mirrorSourceId` | object |  |
| `name` | string |  |
| `nodeId` | string |  |
| `pinned` | boolean |  |
| `pos` | number |  |
| `shortLink` | string |  |
| `shortUrl` | string |  |
| `start` | object |  |
| `subscribed` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Trello API, this operation is `GET lists/:id/cards` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cards-in-a-list.md) for the provider-specific parameters and requirements.

