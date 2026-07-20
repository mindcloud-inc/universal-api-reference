# Chargeflow: Generate Evidence

Generates evidence for an existing dispute in Chargeflow.

```
POST https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/generate-evidence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/generate-evidence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/generate-evidence', {
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
      "account_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "dispute": "string",
      "ext_account_id": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `created_at` | date |  |
| `dispute` | string |  |
| `ext_account_id` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `POST /evidence` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-evidence.md) for the provider-specific parameters and requirements.

