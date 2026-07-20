# Clockify: Get Workspace Time Entry

Retrieves a workspace time entry from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-time-entry?connectionId=$CONNECTION_ID&workspaceId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-time-entry?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `id` | string<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hydrated` | boolean | no | Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "costRate": {
        "amount": 1,
        "currency": "string"
      },
      "customFieldValues": [
        [
          "string"
        ]
      ],
      "description": "string",
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "isLocked": true,
      "timeInterval": {
        "duration": "string",
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "type": "string",
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `costRate` | object |  |
| `costRate.amount` | number |  |
| `costRate.currency` | string |  |
| `customFieldValues[]` | array |  |
| `description` | string |  |
| `hourlyRate` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `timeInterval` | object |  |
| `timeInterval.duration` | string |  |
| `timeInterval.end` | date |  |
| `timeInterval.start` | date |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/time-entries/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-time-entry.md) for the provider-specific parameters and requirements.

