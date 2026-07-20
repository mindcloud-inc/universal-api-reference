# TrackMage: Get Workflow

Retrieves a workflow from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-workflow?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-workflow?${params}`, {
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
| `id` | string | yes | Resource identifier |

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

Through the native TrackMage API, this operation is `GET /workflows/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

