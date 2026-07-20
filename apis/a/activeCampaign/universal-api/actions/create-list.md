# ActiveCampaign: Create List

Creates a new list in ActiveCampaign.

```
POST https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list.name": "Ava Chen",
  "list.stringid": "string",
  "list.sender_url": "https://example.com",
  "list.sender_reminder": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list.name": "Ava Chen",
    "list.stringid": "string",
    "list.sender_url": "https://example.com",
    "list.sender_reminder": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | object | no |  |
| `list.name` | string | yes |  |
| `list.stringid` | string | yes |  |
| `list.sender_url` | string | yes |  |
| `list.sender_reminder` | string | yes |  |
| `list.send_last_broadcast` | boolean | no |  |
| `list.carboncopy` | string | no |  |
| `list.subscription_notify` | string | no |  |
| `list.unsubscription_notify` | string | no |  |
| `list.user` | number | no |  |
| `list.channel` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /lists` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

