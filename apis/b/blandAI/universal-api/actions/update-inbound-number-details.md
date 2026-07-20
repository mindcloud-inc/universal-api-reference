# Bland AI: Update Inbound Number Details

Updates inbound number details in Bland AI.

```
PUT https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-inbound-number-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-inbound-number-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/update-inbound-number-details', {
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
      "failed_updates": [
        {}
      ],
      "message": "string",
      "status": "string",
      "updates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_updates` | array<object> |  |
| `message` | string |  |
| `status` | string |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v1/inbound/{phone_number}` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbound-number-details.md) for the provider-specific parameters and requirements.

