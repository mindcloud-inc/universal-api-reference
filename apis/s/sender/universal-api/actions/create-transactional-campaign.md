# Sender: Create Transactional Campaign



```
POST https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-transactional-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-transactional-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Your receipt",
  "from": "MindCloud",
  "replyTo": "billing@example.com",
  "editor": "html"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-transactional-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Your receipt",
    "from": "MindCloud",
    "replyTo": "billing@example.com",
    "editor": "html"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Name of the campaign shown in reports. Example: `Receipt email`. |
| `subject` | string | yes | Subject line of the campaign. Example: `Your receipt`. |
| `from` | string | yes | Sender name displayed to recipients. Example: `MindCloud`. |
| `replyTo` | string | yes | Sender email. Must belong to a verified domain. Example: `billing@example.com`. |
| `editor` | string | yes | One of plain, html, or builder. Example: `html`. |
| `preheader` | string | no | Preview text of the email. Example: `Order confirmation`. |
| `content` | string | no | Campaign content for plain or html transactional emails. Example: `<p>Your order is confirmed.</p>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "disableClickTracking": true,
      "domainId": "string",
      "editor": "string",
      "from": "string",
      "html": {},
      "id": "string",
      "lastAction": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "preheader": "string",
      "replyTo": "string",
      "subject": "string",
      "title": "string",
      "type": "string",
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
| `created` | date |  |
| `disableClickTracking` | boolean |  |
| `domainId` | string |  |
| `editor` | string |  |
| `from` | string |  |
| `html` | object |  |
| `id` | string |  |
| `lastAction` | string |  |
| `modified` | date |  |
| `preheader` | string |  |
| `replyTo` | string |  |
| `subject` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Sender API, this operation is `POST /transactional` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transactional-campaign.md) for the provider-specific parameters and requirements.

