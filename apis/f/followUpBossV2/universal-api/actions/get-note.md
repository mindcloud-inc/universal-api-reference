# Follow Up Boss: Get Note

Retrieves a note from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-note?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-note?${params}`, {
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
| `id` | string | yes | The note ID. |

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

Through the native Follow Up Boss API, this operation is `GET notes/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

