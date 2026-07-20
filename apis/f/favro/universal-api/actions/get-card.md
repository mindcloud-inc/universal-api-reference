# Favro: Get Card

Retrieves a card from Favro by card ID.

```
GET https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-card?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-card?${params}`, {
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
| `cardId` | string | yes | The Favro card ID to retrieve. |

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

Through the native Favro API, this operation is `GET /cards/:cardId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card.md) for the provider-specific parameters and requirements.

