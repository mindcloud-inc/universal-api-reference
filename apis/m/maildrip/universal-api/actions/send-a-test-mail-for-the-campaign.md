# Maildrip: Send a test mail for the campaign



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-test-mail-for-the-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-test-mail-for-the-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-test-mail-for-the-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invalidEmails": [
        "ava@example.com"
      ],
      "message": "string",
      "sentTo": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invalidEmails` | array<string> |  |
| `message` | string |  |
| `sentTo` | array<string> |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/campaigns/{campaignId}/send-test-mail` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-test-mail-for-the-campaign.md) for the provider-specific parameters and requirements.

