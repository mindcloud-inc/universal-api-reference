# Sender: List Transactional Campaigns



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-transactional-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-transactional-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-transactional-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Sender API, this operation is `GET /transactional` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactional-campaigns.md) for the provider-specific parameters and requirements.

