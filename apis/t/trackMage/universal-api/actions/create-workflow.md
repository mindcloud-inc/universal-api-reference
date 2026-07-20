# TrackMage: Create Workflow

Creates a new workflow in TrackMage.

```
POST https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "string",
  "workspace": "string",
  "enabled": "true",
  "period": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "string",
    "workspace": "string",
    "enabled": "true",
    "period": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `type` | string | yes |  |
| `workspace` | string | yes |  |
| `enabled` | boolean | yes | Default: `true`. |
| `period` | string | yes | applies only to out |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentials.type` | string | no |  |
| `credentials.team` | string | no |  |
| `notificationEmails[]` | array<string> | no |  |
| `integration` | object | no |  |
| `firstTimeSetupPassed` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": "string",
      "enabled": true,
      "firstTimeSetupPassed": true,
      "firstTimeSetupRequired": true,
      "id": "string",
      "integration": {},
      "integrationType": "string",
      "lastRunDate": "2026-05-07T12:00:00.000Z",
      "notificationEmails": [
        "ava@example.com"
      ],
      "passive": true,
      "period": "string",
      "remote": true,
      "runInProgress": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | string |  |
| `enabled` | boolean |  |
| `firstTimeSetupPassed` | boolean |  |
| `firstTimeSetupRequired` | boolean |  |
| `id` | string |  |
| `integration` | object |  |
| `integrationType` | string |  |
| `lastRunDate` | date |  |
| `notificationEmails` | array<string> |  |
| `passive` | boolean |  |
| `period` | string |  |
| `remote` | boolean |  |
| `runInProgress` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `POST /workflows` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

