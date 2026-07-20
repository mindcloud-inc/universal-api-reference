# Process Plan: Get Start Date for Scheduleds in Automated Action Calculate Nexts



```
POST https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-start-date-for-scheduleds-in-automated-action-calculate-nexts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-start-date-for-scheduleds-in-automated-action-calculate-nexts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-start-date-for-scheduleds-in-automated-action-calculate-nexts', {
  method: 'POST',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `POST /automated_action_calculate_next/scheduled/start_date` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-start-date-for-scheduleds-in-automated-action-calculate-nexts.md) for the provider-specific parameters and requirements.

