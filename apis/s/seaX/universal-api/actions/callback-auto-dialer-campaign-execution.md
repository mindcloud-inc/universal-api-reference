# SeaX: Callback Auto Dialer Campaign Execution



```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/callback-auto-dialer-campaign-execution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/callback-auto-dialer-campaign-execution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/callback-auto-dialer-campaign-execution', {
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

```json
{
  "success": true,
  "data": [
    {
      "answered_by": {},
      "attempt": 1,
      "created_time": "string",
      "end_time": "string",
      "id": "string",
      "logs": "string",
      "sequence": 1,
      "start_time": "string",
      "status": {},
      "updated_time": "string",
      "user_account": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answered_by` | object |  |
| `attempt` | number |  |
| `created_time` | string |  |
| `end_time` | string |  |
| `id` | string |  |
| `logs` | string |  |
| `sequence` | number |  |
| `start_time` | string |  |
| `status` | object |  |
| `updated_time` | string |  |
| `user_account` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/execution_callback` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/callback-auto-dialer-campaign-execution.md) for the provider-specific parameters and requirements.

