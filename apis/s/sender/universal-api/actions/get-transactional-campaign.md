# Sender: Get Transactional Campaign



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-transactional-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-transactional-campaign?connectionId=$CONNECTION_ID&id=trn_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "trn_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-transactional-campaign?${params}`, {
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
| `id` | string | yes | Transactional campaign ID. Example: `trn_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "bounced": 1,
      "clicks": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "disableClickTracking": true,
      "domainId": "string",
      "editor": "string",
      "from": "string",
      "html": {},
      "id": "string",
      "lastAction": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "opens": 1,
      "preheader": "string",
      "replyTo": "string",
      "sent": 1,
      "subject": "string",
      "title": "string",
      "type": "string",
      "unsubscribeCount": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `bounced` | number |  |
| `clicks` | number |  |
| `created` | date |  |
| `disableClickTracking` | boolean |  |
| `domainId` | string |  |
| `editor` | string |  |
| `from` | string |  |
| `html` | object |  |
| `id` | string |  |
| `lastAction` | string |  |
| `modified` | date |  |
| `opens` | number |  |
| `preheader` | string |  |
| `replyTo` | string |  |
| `sent` | number |  |
| `subject` | string |  |
| `title` | string |  |
| `type` | string |  |
| `unsubscribeCount` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Sender API, this operation is `GET /transactional/:id` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transactional-campaign.md) for the provider-specific parameters and requirements.

