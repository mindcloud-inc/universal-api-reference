# VoiceGenie: Remove Customer from Campaign

Removes a customer from a VoiceGenie campaign.

```
PUT https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/remove-customer-from-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceGenie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/remove-customer-from-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "customerNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/remove-customer-from-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "customerNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Campaign identifier to update. |
| `customerNumber` | string | yes | Customer number in E.164 format with a leading + and no spaces or punctuation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message returned for the remove-customer request. |
| `success` | boolean | Whether VoiceGenie accepted the remove-customer request. |

## Native endpoint

Through the native VoiceGenie API, this operation is `PUT /publicRestApiActions/pullCustomerFromCampaign` (base URL `https://core-saas.voicegenie.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-customer-from-campaign.md) for the provider-specific parameters and requirements.

