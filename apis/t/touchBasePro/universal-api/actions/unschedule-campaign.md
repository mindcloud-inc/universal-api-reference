# TouchBasePro: Unschedule Campaign

Unschedules an existing campaign in TouchBasePro.

```
PUT https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/unschedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/unschedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/unschedule-campaign', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TouchBasePro API returns.

## Native endpoint

Through the native TouchBasePro API, this operation is `POST /email/campaigns/{campaignId}/unschedule` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unschedule-campaign.md) for the provider-specific parameters and requirements.

