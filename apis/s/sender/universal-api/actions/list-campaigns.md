# Sender: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-campaigns?${params}`, {
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
| `status[]` | array<string> | no | Filter campaigns by status: SCHEDULED, SENDING, SENT, or DRAFT. Example: `DRAFT,SENT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncesCount": 1,
      "clicks": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "domainId": "string",
      "editor": "string",
      "from": "string",
      "html": {},
      "id": "string",
      "language": "string",
      "lastAction": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "opens": 1,
      "preheader": "string",
      "recipientCount": 1,
      "replyTo": "string",
      "reports": {},
      "scheduleTime": "2026-05-07T12:00:00.000Z",
      "sentCount": 1,
      "sentTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncesCount` | number |  |
| `clicks` | number |  |
| `created` | date |  |
| `domainId` | string |  |
| `editor` | string |  |
| `from` | string |  |
| `html` | object |  |
| `id` | string |  |
| `language` | string |  |
| `lastAction` | string |  |
| `modified` | date |  |
| `opens` | number |  |
| `preheader` | string |  |
| `recipientCount` | number |  |
| `replyTo` | string |  |
| `reports` | object |  |
| `scheduleTime` | date |  |
| `sentCount` | number |  |
| `sentTime` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Sender API, this operation is `GET /campaigns` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

