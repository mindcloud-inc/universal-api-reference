# Sender: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Welcome to our launch",
  "from": "MindCloud",
  "replyTo": "hello@example.com",
  "contentType": "html"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Welcome to our launch",
    "from": "MindCloud",
    "replyTo": "hello@example.com",
    "contentType": "html"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Name of the campaign shown in reports. Example: `Spring launch`. |
| `subject` | string | yes | Choose the subject of the campaign. Example: `Welcome to our launch`. |
| `from` | string | yes | Sender name to be shown to subscribers. Example: `MindCloud`. |
| `replyTo` | string | yes | Verified reply-to email address. Example: `hello@example.com`. |
| `contentType` | string | yes | One of editor, html, or text. Example: `html`. |
| `preheader` | string | no | Email preview text. Example: `Preview text`. |
| `groups[]` | array<string> | no | Group IDs that the campaign will be sent to. Example: `grp_123,grp_456`. |
| `segments[]` | array<string> | no | Segment IDs that the campaign will be sent to. Example: `seg_123,seg_456`. |
| `content` | string | no | Campaign content for html or text campaigns. Example: `<p>Hello world</p>`. |

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

Through the native Sender API, this operation is `POST /campaigns` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

