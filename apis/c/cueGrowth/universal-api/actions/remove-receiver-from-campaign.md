# CueGrowth: Remove Receiver From Campaign



```
PUT https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/remove-receiver-from-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/remove-receiver-from-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "linkedinUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/remove-receiver-from-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "linkedinUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | ID of the CSV campaign. |
| `linkedinUrl` | string | yes | LinkedIn URL of the receiver. |
| `email` | string | no | Email of the receiver. |
| `externalId` | string | no | External CRM ID of the receiver. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CueGrowth API returns.

## Native endpoint

Through the native CueGrowth API, this operation is `POST /actions/remove_receiver_from_campaign` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-receiver-from-campaign.md) for the provider-specific parameters and requirements.

