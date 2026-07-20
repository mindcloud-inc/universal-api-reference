# Spoki: Create Automation

Creates an automation with steps, triggers, and optional automation groups.

```
POST https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-automation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the automation. |
| `isActive` | boolean | no | Whether the automation should start active immediately. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | no | Optional advanced automation fields to merge into the provider request body, including steps, triggers, groups, and other supported Spoki fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automationGroups": [
        {}
      ],
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "firstMessageText": "string",
      "id": 1,
      "isActive": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "updatedDatetime": "2026-05-07T12:00:00.000Z",
      "updatedUser": {},
      "webhookSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automationGroups` | array<object> |  |
| `createdDatetime` | date |  |
| `firstMessageText` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `updatedDatetime` | date |  |
| `updatedUser` | object |  |
| `webhookSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `POST /automations/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-automation.md) for the provider-specific parameters and requirements.

