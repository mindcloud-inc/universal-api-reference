# Favro: Create Card

Creates a new card in Favro.

```
POST https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "columnId": "string",
  "name": "Ava Chen",
  "widgetCommonId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnId": "string",
    "name": "Ava Chen",
    "widgetCommonId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columnId` | string | yes | The column ID where the card will be created. |
| `name` | string | yes | The card name. |
| `widgetCommonId` | string | yes | The widget common ID where the card will be created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assignments": [
        "string"
      ],
      "attachments": [
        "string"
      ],
      "cardCommonId": "string",
      "cardId": "string",
      "columnId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": "string",
      "customFields": [
        {}
      ],
      "dependencies": [
        "string"
      ],
      "favroAttachments": [
        "string"
      ],
      "isLane": true,
      "listPosition": 1,
      "name": "Ava Chen",
      "organizationId": "string",
      "position": 1,
      "sequentialId": 1,
      "sheetPosition": 1,
      "tags": [
        "string"
      ],
      "tasksDone": 1,
      "tasksTotal": 1,
      "timeOnBoard": {},
      "timeOnColumns": {},
      "widgetCommonId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `assignments` | array |  |
| `attachments` | array |  |
| `cardCommonId` | string |  |
| `cardId` | string |  |
| `columnId` | string |  |
| `createdAt` | date |  |
| `createdByUserId` | string |  |
| `customFields` | array<object> |  |
| `dependencies` | array |  |
| `favroAttachments` | array |  |
| `isLane` | boolean |  |
| `listPosition` | number |  |
| `name` | string |  |
| `organizationId` | string |  |
| `position` | number |  |
| `sequentialId` | number |  |
| `sheetPosition` | number |  |
| `tags` | array |  |
| `tasksDone` | number |  |
| `tasksTotal` | number |  |
| `timeOnBoard` | object |  |
| `timeOnColumns` | object |  |
| `widgetCommonId` | string |  |

## Native endpoint

Through the native Favro API, this operation is `POST /cards` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

