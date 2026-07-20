# Clockify: List Created Entities (Experimental)

Lists experimentally tracked created entities in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-created-entities-experimental
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-created-entities-experimental?connectionId=$CONNECTION_ID&workspaceId=string&type%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "type[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-created-entities-experimental?${params}`, {
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
| `type[]` | array<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | no | Example: `2026-01-01`. |
| `start` | string | no | Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "auditMetadata": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "billable": true,
      "description": "string",
      "documentType": "string",
      "id": "string",
      "tagIds": [
        [
          "string"
        ]
      ],
      "timeInterval": {
        "duration": "string",
        "end": "2026-05-07T12:00:00.000Z",
        "offsetEnd": 1,
        "offsetStart": 1,
        "start": "2026-05-07T12:00:00.000Z",
        "timeZone": "string",
        "zonedEnd": "2026-05-07T12:00:00.000Z",
        "zonedStart": "2026-05-07T12:00:00.000Z"
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
| `approvalStatus` | string |  |
| `auditMetadata` | object |  |
| `auditMetadata.createdAt` | date |  |
| `auditMetadata.updatedAt` | date |  |
| `billable` | boolean |  |
| `description` | string |  |
| `documentType` | string |  |
| `id` | string |  |
| `tagIds[]` | array |  |
| `timeInterval` | object |  |
| `timeInterval.duration` | string |  |
| `timeInterval.end` | date |  |
| `timeInterval.offsetEnd` | number |  |
| `timeInterval.offsetStart` | number |  |
| `timeInterval.start` | date |  |
| `timeInterval.timeZone` | string |  |
| `timeInterval.zonedEnd` | date |  |
| `timeInterval.zonedStart` | date |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/entities/created` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-created-entities-experimental.md) for the provider-specific parameters and requirements.

