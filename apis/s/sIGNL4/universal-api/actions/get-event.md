# SIGNL4: Get Event

Retrieves an event from SIGNL4 by ID.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | Event id for the event you want to get |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | number | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledgedAlerts": [
        "string"
      ],
      "closedAlerts": [
        "string"
      ],
      "createdByUserId": "string",
      "createdByUserName": "Ava Chen",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "eventSourceGroupId": "string",
      "eventSourceId": "string",
      "eventSourceTeamId": "string",
      "eventSourceType": 1,
      "eventStatus": 1,
      "externalId": "string",
      "from": "string",
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "parameters": {
        "id": "string",
        "name": "Ava Chen",
        "options": 1,
        "order": 1,
        "type": 1,
        "value": "string"
      },
      "processingLog": [
        {}
      ],
      "severity": 1,
      "targets": {
        "alertId": "string",
        "categoryId": "string",
        "creationTime": "2026-05-07T12:00:00.000Z",
        "distributionId": "string",
        "eventId": "string",
        "eventTargetStatus": 1,
        "id": "string",
        "lastModified": "2026-05-07T12:00:00.000Z",
        "teamId": "string"
      },
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
| `closedAlerts` | array<string> |  |
| `createdByUserId` | string |  |
| `createdByUserName` | string |  |
| `creationTime` | date |  |
| `eventSourceGroupId` | string |  |
| `eventSourceId` | string |  |
| `eventSourceTeamId` | string |  |
| `eventSourceType` | number |  |
| `eventStatus` | number |  |
| `externalId` | string |  |
| `from` | string |  |
| `id` | string |  |
| `lastModified` | date |  |
| `parameters` | array<object> |  |
| `parameters.id` | string |  |
| `parameters.name` | string |  |
| `parameters.options` | number |  |
| `parameters.order` | number |  |
| `parameters.type` | number |  |
| `parameters.value` | string |  |
| `processingLog` | array<object> |  |
| `severity` | number |  |
| `targets` | array<object> |  |
| `targets.alertId` | string |  |
| `targets.categoryId` | string |  |
| `targets.creationTime` | date |  |
| `targets.distributionId` | string |  |
| `targets.eventId` | string |  |
| `targets.eventTargetStatus` | number |  |
| `targets.id` | string |  |
| `targets.lastModified` | date |  |
| `targets.teamId` | string |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/events/{eventId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

