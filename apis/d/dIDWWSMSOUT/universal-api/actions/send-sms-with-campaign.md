# DIDWW SMS OUT: Send SMS With Campaign

Creates an outbound SMS in DIDWW SMS OUT with a campaign ID.

```
POST https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DIDWW SMS OUT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "content": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "content": "string",
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | Recipient number in E.164 format. |
| `content` | string | yes | SMS body text. |
| `campaignId` | string | yes | Campaign UUID used when source is omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string | Created outbound message identifier. |
| `data.type` | string | JSON:API resource type. |

## Native endpoint

Through the native DIDWW SMS OUT API, this operation is `POST /outbound_messages` (base URL `https://us.sms-out.didww.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-with-campaign.md) for the provider-specific parameters and requirements.

