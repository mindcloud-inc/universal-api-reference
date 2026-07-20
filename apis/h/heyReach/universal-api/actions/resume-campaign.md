# Hey Reach: Resume Campaign

Resumes a campaign in Hey Reach.

```
PUT https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/resume-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/resume-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/resume-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hey Reach API returns.

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/campaign/Resume` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-campaign.md) for the provider-specific parameters and requirements.

