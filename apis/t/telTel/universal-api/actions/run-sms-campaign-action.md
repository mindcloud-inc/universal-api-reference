# TelTel: Run SMS Campaign Action

Performs an action on an SMS campaign in TelTel.

```
PUT https://connect.mindcloud.co/v1/universal/telTel/latest/actions/run-sms-campaign-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/run-sms-campaign-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/telTel/latest/actions/run-sms-campaign-action', {
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
      "meta": {
        "action": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.action` | string |  |
| `meta.status` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `POST /sms/campaigns/{id}/actions` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-sms-campaign-action.md) for the provider-specific parameters and requirements.

