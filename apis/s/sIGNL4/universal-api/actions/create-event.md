# SIGNL4: Create Event

Creates an event in SIGNL4.

```
POST https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookIdOrTeamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookIdOrTeamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookIdOrTeamId` | string | yes | Use team id to send an event straight to the team or an inbound webhook identifier (https://connect.signl4.com/webhook/{Identifier}) to use distribution rules |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ExtIdParam` | string | no |  |
| `ExtStatusParam` | string | no |  |
| `NewStatus` | string | no |  |
| `ResolvedStatus` | string | no |  |
| `AckStatus` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledgedAlerts": [
        "string"
      ],
      "alertId": "string",
      "categoryId": "string",
      "closedAlerts": [
        "string"
      ],
      "createdByUserId": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "eventSourceGroupId": "string",
      "eventSourceId": "string",
      "eventSourceTeamId": "string",
      "eventSourceType": 1,
      "eventStatus": 1,
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "severity": 1,
      "teamId": "string",
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledgedAlerts` | array<string> |  |
| `alertId` | string |  |
| `categoryId` | string |  |
| `closedAlerts` | array<string> |  |
| `createdByUserId` | string |  |
| `creationTime` | date |  |
| `eventSourceGroupId` | string |  |
| `eventSourceId` | string |  |
| `eventSourceTeamId` | string |  |
| `eventSourceType` | number |  |
| `eventStatus` | number |  |
| `id` | string |  |
| `lastModified` | date |  |
| `severity` | number |  |
| `teamId` | string |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/events/{webhookIdOrTeamId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

