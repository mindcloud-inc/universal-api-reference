# YepCode: Schedule process

Creates a scheduled process in YepCode.

```
POST https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/schedule-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/schedule-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/schedule-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes |  |
| `cron` | string | no |  |
| `allowConcurrentExecutions` | boolean | no |  |
| `dateTime` | string | no |  |
| `input.parameters` | string | no |  |
| `input.comment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "cron": "string",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "paused": true,
      "processId": "string",
      "settings": {
        "agentPoolSlugs": [
          "string"
        ],
        "allowConcurrentExecutions": true
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `cron` | string |  |
| `dateTime` | date |  |
| `id` | string |  |
| `paused` | boolean |  |
| `processId` | string |  |
| `settings.agentPoolSlugs` | array<string> |  |
| `settings.allowConcurrentExecutions` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native YepCode API, this operation is `POST /processes/:identifier/schedule` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-process.md) for the provider-specific parameters and requirements.

