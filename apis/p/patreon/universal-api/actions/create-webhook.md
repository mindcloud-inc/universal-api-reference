# Patreon: Create Webhook

Creates a webhook for the current Patreon campaign.

```
POST https://connect.mindcloud.co/v1/universal/patreon/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Patreon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "triggers[]": [
    "string"
  ],
  "uri": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/patreon/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "triggers[]": ["string"],
    "uri": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The Patreon campaign ID that should trigger the webhook. |
| `triggers[]` | array<string> | yes | The Patreon webhook events to subscribe to. |
| `uri` | string | yes | The fully qualified URL that Patreon should call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Patreon API, this operation is `POST /webhooks` (base URL `https://www.patreon.com/api/oauth2/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

