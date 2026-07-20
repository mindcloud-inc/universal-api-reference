# Week Plan: Extend User Trial



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/extend-user-trial
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/extend-user-trial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/extend-user-trial', {
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

```json
{
  "success": true,
  "data": [
    {
      "Plan": "string",
      "success": true,
      "TrialEndsAt": "string",
      "UserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Plan` | string |  |
| `success` | boolean |  |
| `TrialEndsAt` | string |  |
| `UserId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST users/extend_trial/:userId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-user-trial.md) for the provider-specific parameters and requirements.

