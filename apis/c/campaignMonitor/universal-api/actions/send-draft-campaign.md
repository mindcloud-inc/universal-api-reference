# Campaign Monitor: Send Draft Campaign

Sends a draft campaign in Campaign Monitor.

```
PUT https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/send-draft-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/send-draft-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "confirmationEmail": "ava@example.com",
  "sendDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/send-draft-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "confirmationEmail": "ava@example.com",
    "sendDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Campaign Monitor campaign identifier. |
| `confirmationEmail` | string | yes | Email address to receive the send confirmation. |
| `sendDate` | string | yes | Date and time to send the campaign, or Immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Empty string on success because Campaign Monitor documents HTTP 200 OK with no response body for sending a draft campaign. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `POST /campaigns/:campaignId/send.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-draft-campaign.md) for the provider-specific parameters and requirements.

