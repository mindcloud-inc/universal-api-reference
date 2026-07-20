# Sarbacane: Send Campaign

Sends an existing campaign in Sarbacane.

```
PUT https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/send-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/send-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/send-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | no | Sarbacane campaign ID. |
| `requestedSendDate` | string | no | ISO timestamp for the requested send date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webcopy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webcopy` | string | Webcopy URL returned after scheduling the send. |

## Native endpoint

Through the native Sarbacane API, this operation is `POST /campaigns/{campaignId}/send` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-campaign.md) for the provider-specific parameters and requirements.

