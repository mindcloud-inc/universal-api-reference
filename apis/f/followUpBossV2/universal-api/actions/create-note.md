# Follow Up Boss: Create Note

Creates a new note in Follow Up Boss.

```
POST https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | number | no |  |
| `body` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionPlanId": 1,
      "automationId": 1,
      "body": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdById": 1,
      "id": 1,
      "isExternal": true,
      "isHtml": true,
      "personId": 1,
      "showContent": true,
      "subject": "string",
      "systemId": 1,
      "systemName": "Ava Chen",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "updatedById": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionPlanId` | number |  |
| `automationId` | number |  |
| `body` | string |  |
| `created` | date |  |
| `createdBy` | string |  |
| `createdById` | number |  |
| `id` | number |  |
| `isExternal` | boolean |  |
| `isHtml` | boolean |  |
| `personId` | number |  |
| `showContent` | boolean |  |
| `subject` | string |  |
| `systemId` | number |  |
| `systemName` | string |  |
| `type` | string |  |
| `updated` | date |  |
| `updatedBy` | string |  |
| `updatedById` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `POST notes` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

