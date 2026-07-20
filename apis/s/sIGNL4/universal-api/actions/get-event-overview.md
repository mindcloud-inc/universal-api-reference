# SIGNL4: Get Event Overview

Retrieves an event overview from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-overview?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-overview?${params}`, {
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
| `eventId` | string | yes | Id of event to get. |

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

Through the native SIGNL4 API, this operation is `GET /v2/events/{eventId}/overview` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-overview.md) for the provider-specific parameters and requirements.

